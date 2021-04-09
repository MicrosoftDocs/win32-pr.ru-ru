---
description: Указывает качество кодирования для приемника мультимедиа Digital живая Network Alliance (DLNA).
ms.assetid: 4cf745ab-66ae-40f2-b5c4-3f72f1b9badb
title: Атрибут MF_MP2DLNA_ENCODE_QUALITY (Mfmp2dlna. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81c785ff12524d45d096d566014a5c0a5e24eea8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104080870"
---
# <a name="mf_mp2dlna_encode_quality-attribute"></a>\_ \_ Атрибут качества шифрования MF MP2DLNA \_

Указывает качество кодирования для приемника мультимедиа Digital живая Network Alliance (DLNA).

## <a name="data-type"></a>Тип данных

**UINT32**

Диапазон: 0 – 18

## <a name="getset"></a>Get/Set

Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Комментарии

Большее число указывает на лучшее качество кодирования. Меньшие числа указывают на ускорение кодирования, но с более низким качеством кодирования. Значение по умолчанию — 9.

Чтобы задать этот атрибут для приемника мультимедиа DLNA, запросите приемник мультимедиа для интерфейса [**имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) . Задайте атрибут перед началом потоковой передачи.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>                                             |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2008 R2 \[\]<br/>                                |
| Header<br/>                   | <dl> <dt>Mfmp2dlna. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




