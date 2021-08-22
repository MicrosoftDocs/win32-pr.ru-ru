---
description: Указывает, использует ли приемник мультимедиа Digital живая Network Alliance (DLNA) службу планировщика классов мультимедиа (MMCSS).
ms.assetid: 4c27e2ec-624a-4b1f-bea9-3aaad1534c9b
title: Атрибут MF_MP2DLNA_USE_MMCSS (Mfmp2dlna. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79e824451be89bf4aca485edd2c61ce381f0cf4e0a9d5eefff82bf6c99cef2eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119104760"
---
# <a name="mf_mp2dlna_use_mmcss-attribute"></a>MF \_ MP2DLNA \_ использовать \_ атрибут MMCSS

Указывает, использует ли приемник мультимедиа Digital живая Network Alliance (DLNA) службу планировщика классов мультимедиа (MMCSS).

## <a name="data-type"></a>Тип данных

**Bool** , сохраненный как **UINT32**

## <a name="getset"></a>Get/Set

Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Remarks

Чтобы задать этот атрибут для приемника мультимедиа DLNA, запросите приемник мультимедиа для интерфейса [**имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) . Задайте атрибут перед началом потоковой передачи.

Если этот атрибут имеет **значение true**, приемник мультимедиа DLNA регистрируется в службе MMCSS.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                             |
| Минимальная версия сервера<br/> | Windows \[Только для настольных приложений сервера 2008 R2\]<br/>                                |
| Header<br/>                   | <dl> <dt>Mfmp2dlna. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




