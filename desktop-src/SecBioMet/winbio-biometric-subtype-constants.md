---
title: Константы WINBIO_BIOMETRIC_SUBTYPE (Винбио \_ types. h)
description: Укажите сведения о биометрического измерения.
ms.assetid: 019569A9-6184-4E75-9B82-C98F4F45F61A
topic_type:
- apiref
api_name:
- WINBIO_SUBTYPE_NO_INFORMATION
- WINBIO_SUBTYPE_ANY
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba1bc25337bf49a48b54b6b2426673daf8a15bd9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988877"
---
# <a name="winbio_biometric_subtype-constants"></a>\_Константы ПОДтипа БИОметрической метрики винбио \_

**Винбио \_ Константы \_ ПОДтипа БИОметрической метрики** используются во всех биометрическая платформа Windows для предоставления дополнительных сведений о биометрических измерениях. Следующие константы можно использовать, если ни один подтип не является обязательным или если требуется какой-либо подтип.



| Константа/значение                                                                                                                                                                                                                                                            | Описание                        |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------|
| <span id="WINBIO_SUBTYPE_NO_INFORMATION"></span><span id="winbio_subtype_no_information"></span><dl> <dt>**Винбио \_ ПОДТИП \_ нет \_ сведений**</dt> <dt>0x00</dt> </dl> | Нет сведений о подтипе.<br/> |
| <span id="WINBIO_SUBTYPE_ANY"></span><span id="winbio_subtype_any"></span><dl> <dt>**Винбио \_ ПОДТИП \_ любой**</dt> <dt>0xFF</dt> </dl>                                   | Любой подтип.<br/>            |



## <a name="remarks"></a>Комментарии

Чтобы найти доступные биометрические подтипы для конкретного биометрического типа, используйте следующую таблицу:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>WINBIO_BIOMETRIC_TYPE</strong> значение</th>
<th>Разделы для поиска <strong>WINBIO_BIOMETRIC_SUBTYPE</strong> значений</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>WINBIO_TYPE_FACIAL_FEATURES</strong></td>
<td><a href="winbio-ansi-385-face-constants.md"><strong>Константы WINBIO_ANSI_385_FACE</strong></a>
<blockquote>
[!Note]<br />
Эти значения применяются только к Windows 10 и более поздним версиям.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><strong>WINBIO_TYPE_FINGERPRINT</strong></td>
<td>Один из следующих разделов:
<ul>
<li><a href="winbio-ansi-381-format-constants.md"><strong>Константы WINBIO_ANSI_381_FORMAT</strong></a></li>
<li><a href="winbio-ansi-381-img-constants.md"><strong>Константы WINBIO_ANSI_381_IMG</strong></a></li>
<li><a href="winbio-ansi-381-img-acq-constants.md"><strong>Константы WINBIO_ANSI_381_IMG_ACQ</strong></a></li>
<li><a href="winbio-ansi-381-imp-type-constants.md"><strong>Константы WINBIO_ANSI_381_IMP_TYPE</strong></a></li>
<li><a href="winbio-ansi-381-pixels-constants.md"><strong>Константы WINBIO_ANSI_381_PIXELS</strong></a></li>
<li><a href="winbio-ansi-381-pos-fingerprint-constants.md"><strong>Константы отпечатка WINBIO_ANSI_381_POS</strong></a></li>
<li><a href="winbio-ansi-381-pos-palm-constants.md"><strong>Константы WINBIO_ANSI_381_POS_Palm</strong></a></li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>WINBIO_TYPE_IRIS</strong></td>
<td><a href="winbio-iris-constants.md"><strong>Константы WINBIO_IRIS</strong></a>
<blockquote>
[!Note]<br />
Эти значения применяются только к Windows 10 и более поздним версиям.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><strong>WINBIO_TYPE_VOICE</strong></td>
<td><a href="https://www.bing.com/search?q=<strong>WINBIO_VOICE+Constants</strong>"><strong>Константы WINBIO_VOICE</strong></a>
<blockquote>
[!Note]<br />
Эти значения применяются только к Windows 10 и более поздним версиям.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

Дополнительные сведения см. в разделе [константы клиентского приложения](client-application-constants.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>                                                                    |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2008 R2 \[\]<br/>                                                       |
| Header<br/>                   | <dl> <dt>Винбио \_ types. h (include винбио. h)</dt> </dl> |



 

 





