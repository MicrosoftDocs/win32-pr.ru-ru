---
title: Сопоставление объявлений D3D9 и D3D8
description: Эта таблица сопоставляет члены объявления D3DVERTEXELEMENT9 с объявлением Direct3D 8.
ms.assetid: da02b2cd-5221-4d37-97d5-840df91e39a6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5c52bd804907f201916386ef5fa5776a32a046b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103805314"
---
# <a name="map-between-d3d9-and-d3d8-declarations"></a>Сопоставление объявлений D3D9 и D3D8

Эта таблица сопоставляет члены объявления [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) с объявлением Direct3D 8.



| Использование Direct3D 9           | Индекс использования Direct3D 9 | Direct3D 8            |
|----------------------------|------------------------|-----------------------|
| D3DDECLUSAGEное \_ расположение     | 0                      | D3DVSDEное \_ расположение     |
| D3DDECLUSAGEное \_ расположение     | 1                      | D3DVSDE \_ POSITION2    |
| D3DDECLUSAGE, \_ Обычная       | 0                      | D3DVSDE, \_ Обычная       |
| D3DDECLUSAGE, \_ Обычная       | 1                      | D3DVSDE \_ NORMAL2      |
| D3DDECLUSAGE \_ блендвеигхт  | 0                      | D3DVSDE \_ блендвеигхт  |
| D3DDECLUSAGE \_ блендиндицес | 0                      | D3DVSDE \_ блендиндицес |
| D3DDECLUSAGE \_ псизе        | 0                      | D3DVSDE \_ псизе        |
| \_Цвет D3DDECLUSAGE        | 0                      | D3DVSDE \_ диффузный      |
| \_Цвет D3DDECLUSAGE        | 1                      | \_Зеркальное отражение D3DVSDE     |
| D3DDECLUSAGE \_ текскурд     | n                      | D3DVSDE \_ текскурдн    |



 

Если объявление используется с аппаратной обработкой вершин в драйвере Direct3D 7, среда выполнения Direct3D преобразует ее в ФВФ со следующими правилами:

-   Следует использовать только поток 0 (очевидно от Максстреамс крепления).
-   Порядок элементов вершин должен совпадать с порядком битов ФВФ.
-   Пробелы в координатах текстуры не допускаются.
-   Любой элемент вершины, не описанный в таблице, не может быть преобразован в допустимый ФВФ для всех драйверов, предшествующих DirectX 8, и поэтому не может использоваться для этих драйверов.
-   Только D3DDECLTYPE \_ FLOAT2 разрешен для элементов вершины с D3DDECLUSAGE \_ текскурд, если устройство не устанавливает ни одно из D3DPTEXTURECAPS, \_ либо D3DPTEXTURECAPS \_ кубической карты.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Объявление вершины](vertex-declaration.md)
</dt> </dl>

 

 



