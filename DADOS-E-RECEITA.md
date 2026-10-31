# Alfajores Misky — Datos reales (receta, compras y producción)

**Actualizado:** 26/10/2026, con los datos que pasó Renato.
**Confirmado por Renato (26/10):** el producto correcto es **margarina** — lo que en las compras figuraba como "manteiga" es la margarina (1 kg).
**Unidad de descuento de material = FORNADA (decisión de Renato, 26/10):** los materiales se descuentan por fornada producida, no por venta ni por unidad vendida.

## 1. Receta por LOTE de producción (fornada)

### Galletas del alfajor
| Material | Cantidad por lote | Unidad de stock |
|---|---|---|
| Azúcar | 100 | g |
| Amido de milho (maicena) | 300 | g |
| Farinha de trigo | 350 | g |
| Margarina 50% lipídios | 400 | g |
| Ovo | 1 | unidad |

### Decorado
| Material | Cantidad por lote | Unidad de stock |
|---|---|---|
| Doce de leite | 600 | g |
| Coco ralado | 100 | g |

### Empacotado (variable según producción real)
| Material | Cantidad | Regla |
|---|---|---|
| Saquinho plástico | 1 | por cada paquete producido |
| Fitilho | 10 | cm por cada paquete producido |

## 2. Rendimiento del lote — CLAVE

- Cada fornada rinde **por lo menos 30 paquetes** (corrección de Renato, 26/10 — reemplaza el "60 a 65" dicho antes; el rendimiento real varía).
- Cada paquete = **3 alfajores = 6 tapinhas**.
- La app necesita un campo **«cantidad de paquetes producidos»** al registrar cada producción: con ese número se descuentan el saquinho y el fitilho (por paquete) y se suma esa cantidad al stock de paquetes listos para vender.
- Los ingredientes de la fornada (galletas + decorado) se descuentan **fijos por fornada**; lo que cambia con el rendimiento es el costo por paquete.

## 3. Compras (stock inicial a cargar)

| Material | Cantidad comprada | Unidad de stock |
|---|---|---|
| Azúcar | 1 kg | 1000 g |
| Amido de milho | 1 kg | 1000 g |
| Farinha de trigo | 1 kg | 1000 g |
| Margarina 50% lipídios | 1 kg | 1000 g |
| Ovos | 12 | unidades |
| Doce de leite | 5 kg | 5000 g |
| Coco ralado | 120 g | 120 g |
| Saquinhos plásticos | 100 | unidades |
| Fitilho | 30 m | 3000 cm |

## 4. Capacidad que surge de estas compras (cálculo)

Por fornada se consume: azúcar 100 g (alcanza 10 fornadas), amido 300 g (3), farinha 350 g (2), margarina 400 g (2), ovo 1 (12), doce de leite 600 g (8), coco 100 g (**solo 1 fornada completa** — es el primer cuello de botella), saquinhos 30+ por fornada (~3 fornadas con 100 unidades), fitilho 300+ cm por fornada (hasta 10).

Con estas compras se puede producir **1 fornada completa segura**; el coco ralado es lo primero que se acaba, y después la margarina y la farinha (2 fornadas).
