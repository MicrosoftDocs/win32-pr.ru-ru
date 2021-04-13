---
description: Возвращает статистику для приемника мультимедиа Digital живая Network Alliance (DLNA).
ms.assetid: 1fa6ea9f-fd30-4fa2-a0e6-1647273bcc35
title: Атрибут MF_MP2DLNA_STATISTICS (Mfmp2dlna. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a51620c1ca093a422a5e4657edcfbfaa66ae6cd3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544367"
---
# <a name="mf_mp2dlna_statistics-attribute"></a>\_ \_ Атрибут статистики MF MP2DLNA

Возвращает статистику для приемника мультимедиа Digital живая Network Alliance (DLNA).

## <a name="data-type"></a>Тип данных

**[**MFMPEG2DLNASINKSTATS**](/windows/desktop/api/mfmp2dlna/ns-mfmp2dlna-mfmpeg2dlnasinkstats)** хранится в **виде \[ \] байта**

## <a name="getset"></a>Get/Set

Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес::-BLOB**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).

## <a name="remarks"></a>Комментарии

Во время потоковой передачи приемник мультимедиа DLNA обновляет этот атрибут со статистикой о кодировке и мультиплексировании потоков MPEG-2. Приложение может в любое время запросить этот атрибут для получения последних значений.

Установка этого атрибута для приемника мультимедиа DLNA не оказывает никакого воздействия.

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

 

 




