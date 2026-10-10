# 개념 지도

`concept/`에서 다루는 공식 개념 목록

| 태그 | 개념 | 선행 개념 |
| --- | --- | --- |
| `vector` | [벡터](vector.md) | |
| `scalar` | [스칼라](scalar.md) | |
| `vector-addition` | [벡터 덧셈](vector-addition.md) | 벡터 |
| `scalar-multiplication` | [스칼라곱](scalar-multiplication.md) | 벡터, 스칼라 |
| `zero-vector` | [영벡터](zero-vector.md) | 벡터 |
| `additive-inverse` | [역원](additive-inverse.md) | 벡터, 영벡터 |
| `vector-space` | [벡터공간](vector-space.md) | 벡터, 영벡터, 역원 |
| `linear-combination` | [일차결합](linear-combination.md) | 벡터 |
| `span` | [생성](span.md) | 일차결합 |
| `linear-independence` | [일차독립](linear-independence.md) | 일차결합 |
| `basis` | [기저](basis.md) | 생성, 일차독립 |
| `standard-basis` | [표준기저](standard-basis.md) | 기저 |
| `coordinates` | [좌표](coordinates.md) | 기저 |
| `component` | [성분](component.md) | 좌표 |
| `coordinate-system` | [좌표계](coordinate-system.md) | 기저, 좌표 |
| `dimension` | [차원](dimension.md) | 기저 |
| `inner-product` | [내적](inner-product.md) | 벡터 |
| `orthogonality` | [직교](orthogonality.md) | 내적 |
| `norm` | [노름](norm.md) | 내적 |
| `unit-vector` | [단위벡터](unit-vector.md) | 노름 |
| `normalization` | [정규화](normalization.md) | 단위벡터 |
| `cosine-similarity` | [코사인 유사도](cosine-similarity.md) | 내적, 노름 |
| `vector-projection` | [벡터 정사영](vector-projection.md) | 내적, 노름 |
| `orthogonal-component` | [직교 성분](orthogonal-component.md) | 직교, 벡터 정사영 |
| `orthonormal-basis` | [정규직교기저](orthonormal-basis.md) | 기저, 직교, 단위벡터 |
| `gram-schmidt` | [그람-슈미트 과정](gram-schmidt.md) | 일차독립, 정규화, 벡터 정사영 |
| `matrix` | [행렬](matrix.md) | 스칼라 |
| `matrix-vector-product` | [행렬과 벡터의 곱](matrix-vector-product.md) | 일차결합 |
| `change-of-basis` | [기저변환행렬](change-of-basis.md) | 좌표, 행렬과 벡터의 곱 |
| `subspace` | [부분공간](subspace.md) | 벡터공간 |
| `orthogonal-complement` | [직교여공간](orthogonal-complement.md) | 직교, 부분공간 |
| `orthogonal-projection` | [부분공간으로의 정사영](orthogonal-projection.md) | 정규직교기저, 부분공간, 직교여공간 |
| `linear-transformation` | [선형변환](linear-transformation.md) | 벡터공간 |
| `transformation-matrix` | [선형변환의 행렬](transformation-matrix.md) | 기저, 선형변환 |
| `composition` | [합성](composition.md) | 선형변환 |
| `matrix-product` | [행렬 곱](matrix-product.md) | 선형변환의 행렬, 합성 |
| `identity-matrix` | [단위행렬](identity-matrix.md) | 행렬, 행렬 곱 |
| `inverse-matrix` | [역행렬](inverse-matrix.md) | 행렬 곱 |
| `determinant` | [행렬식](determinant.md) | 선형변환의 행렬 |
| `singular-matrix` | [특이행렬](singular-matrix.md) | 역행렬, 행렬식 |
| `eigenvector` | [고유벡터](eigenvector.md) | 선형변환 |
| `eigenvalue` | [고윳값](eigenvalue.md) | 고유벡터 |
| `eigenspace` | [고유공간](eigenspace.md) | 부분공간, 고윳값 |
| `characteristic-polynomial` | [특성다항식](characteristic-polynomial.md) | 단위행렬, 행렬식, 고윳값 |
| `diagonalization` | [대각화](diagonalization.md) | 기저변환행렬, 고윳값 |
| `transpose` | [전치행렬](transpose.md) | 내적, 선형변환의 행렬 |
| `symmetric-matrix` | [대칭행렬](symmetric-matrix.md) | 전치행렬 |
| `positive-definite` | [양의 정부호 행렬](positive-definite.md) | 행렬과 벡터의 곱, 대칭행렬 |
| `positive-semidefinite` | [양의 준정부호 행렬](positive-semidefinite.md) | 행렬과 벡터의 곱, 대칭행렬 |
| `spectral-theorem` | [스펙트럼 정리](spectral-theorem.md) | 정규직교기저, 대각화, 대칭행렬 |
| `linear-system` | [연립일차방정식](linear-system.md) | 행렬과 벡터의 곱 |
| `gaussian-elimination` | [가우스 소거법](gaussian-elimination.md) | 행렬, 연립일차방정식 |
| `row-echelon-form` | [행 사다리꼴](row-echelon-form.md) | 가우스 소거법 |
| `column-space` | [열공간](column-space.md) | 생성, 선형변환의 행렬 |
| `row-space` | [행공간](row-space.md) | 생성, 행렬, 전치행렬 |
| `null-space` | [영공간](null-space.md) | 부분공간, 선형변환 |
| `left-null-space` | [왼쪽 영공간](left-null-space.md) | 전치행렬, 영공간 |
| `rank` | [계수](rank.md) | 차원, 열공간 |
| `rank-nullity-theorem` | [계수·영차원 정리](rank-nullity-theorem.md) | 차원, 영공간, 계수 |
| `least-squares` | [최소제곱](least-squares.md) | 벡터 정사영, 열공간 |
| `normal-equations` | [정규방정식](normal-equations.md) | 행렬 곱, 전치행렬, 최소제곱 |
| `minimum-norm-solution` | [최소 노름 해](minimum-norm-solution.md) | 노름, 직교여공간, 연립일차방정식, 영공간 |
| `gram-matrix` | [그람 행렬](gram-matrix.md) | 기저, 내적 |
| `linear-functional` | [선형범함수](linear-functional.md) | 선형변환 |
| `pseudoinverse` | [유사역행렬](pseudoinverse.md) | 영공간, 최소제곱 |
| `orthogonal-matrix` | [직교행렬](orthogonal-matrix.md) | 정규직교기저 |
| `singular-value` | [특잇값](singular-value.md) | 노름, 선형변환 |
| `singular-value-decomposition` | [특잇값 분해](singular-value-decomposition.md) | 대각화, 스펙트럼 정리, 직교행렬, 특잇값 |
