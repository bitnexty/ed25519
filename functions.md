# Monero代码中ed25519相关crypto函数对应关系



Monero中ed25519的相关函数对应表：



| Monero                               | golang                             | 说明                   |
| ------------------------------------ | ---------------------------------- | ---------------------- |
| ge_p2                                | ProjectiveGroupElement             | 数据结构，椭圆曲线的点 |
| ge_p3                                | ExtendedGroupElement               |                        |
| ge_p1p1                              | CompletedGroupElement              |                        |
| ge_precomp                           | PreComputedGroupElement            |                        |
| ge_cached                            | CachedGroupElement                 |                        |
| ge_double_scalarmult_base_vartime    | GeDoubleScalarMultVartime          |                        |
| ge_frombytes_vartime                 | FromBytes                          |                        |
| ge_p1p1_to_p2                        | ToProjective                       |                        |
| ge_p1p1_to_p3                        | ToExtended                         |                        |
| ge_p2_dbl                            |                                    |                        |
| ge_p3_to_cached                      | ToCached                           |                        |
| ge_p3_to_p2                          | ToProjective                       |                        |
| ge_p3_tobytes                        | ToBytes                            |                        |
| ge_scalarmult_base                   | GeScalarMultBase                   |                        |
| ge_tobytes                           | (*ProjectiveGroupElement)ToBytes   |                        |
| sc_reduce                            | ScReduce                           |                        |
| ge_scalarmult                        | GeScalarMult                       |                        |
| ge_double_scalarmult_precomp_vartime | GeDoubleScalarMultPrecompVartime   |                        |
| ge_mul8                              | GeMul8                             |                        |
| ge_fromfe_frombytes_vartime          | (*ProjectiveGroupElement)FromBytes |                        |
| sc_0                                 |                                    |                        |
| sc_reduce32                          | ScReduce32                         |                        |
| sc_add                               | ScAdd                              |                        |
| sc_sub                               | ScSub                              |                        |
| sc_mulsub                            | ScMulSub                           |                        |
| sc_check                             | ScValid                            |                        |
| sc_isnonzero                         | ScIsZero                           |                        |
|                                      |                                    |                        |
|                                      |                                    |                        |



## ge开头的函数



## sc开头的函数



