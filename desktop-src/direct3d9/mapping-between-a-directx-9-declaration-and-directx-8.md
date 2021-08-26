---
title: Сопоставление объявлений D3D9 и D3D8
description: Эта таблица сопоставляет члены объявления D3DVERTEXELEMENT9 с объявлением Direct3D 8.
ms.assetid: da02b2cd-5221-4d37-97d5-840df91e39a6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d38e6c94836499a6f2bf5dc4e88c76b822ef3143278581a4020e76dba16c9869
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069034"
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

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Объявление вершины](vertex-declaration.md)
</dt> </dl>

 

 



