---
description: Эта таблица сопоставляет члены объявления D3DVERTEXELEMENT9 с кодом ФВФ.
ms.assetid: be4357b5-5b92-44ca-9100-ec9473930446
title: Сопоставление между объявлением Direct3D и кодами ФВФ (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4831af7b8c03ae4abd5ac2847351d2a6c921fb97
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104139971"
---
# <a name="mapping-between-a-direct3d-declaration-and-fvf-codes-direct3d-9"></a>Сопоставление между объявлением Direct3D и кодами ФВФ (Direct3D 9)

Эта таблица сопоставляет члены объявления [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) с кодом фвф.



| Тип данных             | Использование                      | Индекс использования | фвф                       |
|-----------------------|----------------------------|-------------|---------------------------|
| D3DDECLTYPE \_ FLOAT3   | D3DDECLUSAGEное \_ расположение     | 0           | D3DFVF \_ XYZ               |
| D3DDECLTYPE \_ FLOAT4   | D3DDECLUSAGE \_ позиций    | 0           | D3DFVF \_ ксизрхв            |
| D3DDECLTYPE \_ флоатн   | D3DDECLUSAGE \_ блендвеигхт  | 0           | D3DFVF \_ ксизбн             |
| D3DDECLTYPE \_ UBYTE4   | D3DDECLUSAGE \_ блендиндицес | 0           | D3DFVF \_ ксизб (нвеигхтс + 1) |
| D3DDECLTYPE \_ FLOAT3   | D3DDECLUSAGE, \_ Обычная       | 0           | D3DFVF, \_ Обычная            |
| D3DDECLTYPE \_ FLOAT1   | D3DDECLUSAGE \_ псизе        | 0           | D3DFVF \_ псизе             |
| D3DDECLTYPE \_ D3DCOLOR | \_Цвет D3DDECLUSAGE        | 0           | D3DFVF \_ диффузный           |
| D3DDECLTYPE \_ D3DCOLOR | \_Цвет D3DDECLUSAGE        | 1           | \_Зеркальное отражение D3DFVF          |
| D3DDECLTYPE \_ флоатм   | D3DDECLUSAGE \_ текскурд     | n           | D3DFVF \_ текскурдсизем (n)  |
| D3DDECLTYPE \_ FLOAT3   | D3DDECLUSAGEное \_ расположение     | 1           | Недоступно                       |
| D3DDECLTYPE \_ FLOAT3   | D3DDECLUSAGE, \_ Обычная       | 1           | Недоступно                       |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Объявление вершины](vertex-declaration.md)
</dt> </dl>

 

 



