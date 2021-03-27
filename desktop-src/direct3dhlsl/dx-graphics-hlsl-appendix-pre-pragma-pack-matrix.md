---
title: Директива pragma pack_matrix
description: Директива pragma, задающая выравнивание упаковки для матриц.
ms.assetid: e77dc007-d915-4d78-9fff-d44d4999e4da
keywords:
- pack_matrix директивы pragma HLSL
topic_type:
- apiref
api_name:
- pack_matrix pragma Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4bb5474702a1caba3f772002c34677601715caff
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104068999"
---
# <a name="pack_matrix-pragma-directive"></a>\_директива pragma матрицы Pack

Директива pragma, задающая выравнивание упаковки для матриц.



| \#\_Матрица pragma pack ( *Выравнивание* ) |
|--------------------------------------|



 

## <a name="parameters"></a>Параметры



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Элемент</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="alignment"></span><span id="ALIGNMENT"></span><em>Выравнивание</em><br/></td>
<td>Выравнивание, устанавливаемое для матриц. Этот параметр может принимать одно из значений, перечисленных в следующей таблице. <br/> 
<table>
<thead>
<tr class="header">
<th>Значение</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>column_major</td>
<td>По умолчанию. Задает для выравнивания упаковки матрицы значение столбца Major.</td>
</tr>
<tr class="even">
<td>row_major</td>
<td>Задает выравнивание упаковки матрицы по строке основной.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="examples"></a>Примеры

В следующем примере устанавливается выравнивание упаковки матрицы в строку Major.


```
#pragma pack_matrix( row_major )
```



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Директивы препроцессора (DirectX HLSL)](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[\#Директива pragma (DirectX HLSL)](dx-graphics-hlsl-appendix-pre-pragma.md)
</dt> </dl>

 

 





