# AGN-Flares
1. AGN Flare Coarse Catalog (AGNFCC): AGN flares identified using Gaussian Processes, showing features distinct from AGN variability.
2. AGN Flare Refined Catalog (AGNFRC): A subset AGN flares from the AGNFCC, refined through more stringent criteria.
## Catalog Fields
| Column Name       | Unit             | Description |
|-------------------|------------------|-------------|
| AGN_name          | —                | Name of the host AGN. |
| RA                | deg              | Right ascension. |
| DEC               | deg              | Declination. |
| z                 | —                | Redshift. |
| source            | —                | Source catalog: 'M' for Milliquas, 'D' for DESI, 'L' for LAMOST, 'Q' for Quaia, and 'W' for WISE. |
| type              | —                | Source type, including 'Blazar', 'SN', and 'TDE'. |
| ALeRCE            | —                | Classification result from the ALeRCE. |
| t0                | MJD              | $t_{0}$, peak time of the flare. |
| te                | day              | $t_{e}$, exponential decay timescale of the flare. |
| tg                | day              | $t_{g}$, gaussian rise timescale of the flare. |
| r0\_g             | $\mu \mathrm{Jy}$ | $r_{0g}$, baseline flux density in g band. |
| r0\_r             | $\mu \mathrm{Jy}$ | $r_{0r}$, baseline flux density in r band. |
| A\_g              | $\mu \mathrm{Jy}$ | $A_{g}$, flare amplitude in g band. |
| A\_r              | $\mu \mathrm{Jy}$ | $A_{r}$, flare amplitude in r band. |
| max\_gap          | day              | Maximum observational gap in light curve. |
| peak\_sigma\_g    | —                | Significance level of the peak flux in g band. |
| peak\_sigma\_r    | —                | Significance level of the peak flux in r band. |
| excess\_num\_g    | —                | Number of non-flare points exceeding 3$\sigma$ in g band. |
| excess\_num\_r    | —                | Number of non-flare points exceeding 3$\sigma$ in r band. |
| delta\_bic        | —                | Difference between BIC for the constant model and the flare model. |
| flare\_point\_g   | —                | Number of points within the flare interval $(t_{0}-t_{g}, t_{0}+t_{e})$ in g band. |
| flare\_point\_r   | —                | Number of points within the flare interval $(t_{0}-t_{g}, t_{0}+t_{e})$ in r band. |
| flag\_1           | —                | Boolean flag indicating whether max\_gap $>$ 500 days. |
| flag\_2           | —                | Boolean flag indicating whether min(peak\_sigma\_g, peak\_sigma\_r) $<$ 3. |
| flag\_3           | —                | Boolean flag indicating whether excess\_num\_g + excess\_num\_r $>$ 2. |
| flag\_4           | —                | Boolean flag indicating whether delta\_bic $<$ 10. |
| flag\_5           | —                | Boolean flag indicating whether $t_0 + t_e > \max(\mathrm{MJD})$ or $t_0 - t_g < \min(\mathrm{MJD})$. |
| flag\_6           | —                | Boolean flag indicating whether $\min(\mathrm{flare\_point\_g}, \mathrm{flare\_point\_r}) < (t_g + t_e)/20$. |
| flag\_7           | —                | Boolean flag indicating whether $\min(A_g/r0_g, A_r/r0_r) < 0.2$. |
| flag\_8           | —                | Boolean flag indicating whether this AGN is confused with other sources. |
