---
description: Указывает частоту обновления монитора.
ms.assetid: deeb780c-2dc2-4a9a-926a-23b9ae3bedd5
title: Атрибут MF_TOPOLOGY_PLAYBACK_FRAMERATE (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 620d7ff7dbc893065ebb378557f0731cd8826582
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263616"
---
# <a name="mf_topology_playback_framerate-attribute"></a>\_ \_ Атрибут частоты воспроизведения для топологии MF \_

Указывает частоту обновления монитора.

## <a name="data-type"></a>Тип данных

**UINT64**

## <a name="getset"></a>Get/Set

Чтобы получить этот атрибут, вызовите [**мфжетаттрибутератио**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio).

Чтобы задать этот атрибут, вызовите [**мфсетаттрибутератио**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributeratio).

## <a name="applies-to"></a>Применяется к

[**имфтопологи**](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a>Комментарии

Загрузчик топологии использует этот атрибут для оптимизации конвейера перед началом воспроизведения. Если этот атрибут задан, также установите для атрибута [" \_ \_ \_ \_ Оптимизация воспроизведения статических топологий MF](mf-topology-static-playback-optimizations.md) " **значение true**.

Частота кадров выражается в виде коэффициента. Верхние 32 бит значения атрибута содержат числитель, а младшие 32 биты содержат знаменатель.

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>                                         |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2008 R2 \[\]<br/>                            |
| Header<br/>                   | <dl> <dt>Мфидл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Атрибуты топологии](topology-attributes.md)
</dt> <dt>

[Управление качеством видео](video-quality-management.md)
</dt> </dl>

 

 




