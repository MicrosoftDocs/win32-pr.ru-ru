---
description: Флаг возможностей драйвера.
ms.assetid: 78ff4433-f0b5-4bbb-b2c0-bd389fbc31ce
title: D3DENUM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50cb3ed10a4a12602e8586bbd0e941641287346a
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2021
ms.locfileid: "122628000"
---
# <a name="d3denum"></a>D3DENUM

Флаг возможностей драйвера.



<table>
<colgroup>
<col  />
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>#определенно</td>
<td>Значение</td>
<td>Описание:</td>
</tr>
<tr class="even">
<td>D3DENUM_WHQL_LEVEL</td>
<td>0x00000002L</td>
<td>тестирование драйвера лаборатории WHQL (майкрософт Windows). Это длительный тест, требующий снижения времени на одну секунду или две секунды. Эта константа используется членом Вхкллевел <a href="d3dadapter-identifier9.md"><strong>D3DADAPTER_IDENTIFIER9</strong></a>.<br/> 
<table>
<tbody>
<tr class="odd">
<td>Различия между Direct3D 9 и Direct3D 9Ex:<br/> D3DENUM_WHQL_LEVEL не рекомендуется использовать для Direct3D9Ex, работающих в Windows Vista, Windows server 2008, Windows 7 и Windows Server 2008 R2 (или более текущей операционной системы). Любая из этих операционных систем возвращает 1 для уровня WHQL без проверки состояния драйвера. <br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="constant-information"></a>Сведения о константе



| Требование                         | Значение           |
|--------------------------|------------|
| Заголовок                   | d3d9. h     |
| Минимальная операционная система | Windows 98 |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Константы Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 




