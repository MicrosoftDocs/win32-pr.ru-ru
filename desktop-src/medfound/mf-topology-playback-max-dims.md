---
description: Задает размер окна назначения для воспроизведения видео.
ms.assetid: 46af4c11-042c-4580-ba9d-3aee6172de56
title: Атрибут MF_TOPOLOGY_PLAYBACK_MAX_DIMS (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d1fc6a57c5e031bc6f35f36e688bd44986f541b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263615"
---
# <a name="mf_topology_playback_max_dims-attribute"></a>\_ \_ Максимальный размер для воспроизведения топологии \_ MF \_

Задает размер окна назначения для воспроизведения видео.

## <a name="data-type"></a>Тип данных

**UINT64**

## <a name="getset"></a>Get/Set

Чтобы получить этот атрибут, вызовите [**мфжетаттрибутесизе**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributesize).

Чтобы задать этот атрибут, вызовите [**мфсетаттрибутесизе**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributesize).

## <a name="applies-to"></a>Применяется к

[**имфтопологи**](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a>Комментарии

Загрузчик топологии использует этот атрибут для оптимизации конвейера перед началом воспроизведения. Если этот атрибут задан, также установите для атрибута [" \_ \_ \_ \_ Оптимизация воспроизведения статических топологий MF](mf-topology-static-playback-optimizations.md) " **значение true**.

Верхние 32 бит значения атрибута содержат ширину, а младшие 32 бита содержат высоту в пикселях.

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

 

 




