---
description: Указывает, поддерживает ли преобразование Media Foundation (MFT) Microsoft Direct3D 11.
ms.assetid: 23482B8A-58F3-4B39-9C6D-54EC27D36C01
title: Атрибут MF_SA_D3D11_AWARE (Мфтрансформ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d90f560e3d31b80c1b3fbcbb5c25c4e20815f51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344175"
---
# <a name="mf_sa_d3d11_aware-attribute"></a>\_Атрибут MF SA \_ D3D11 с \_ поддержкой

Указывает, поддерживает ли преобразование Media Foundation (MFT) Microsoft Direct3D 11.

## <a name="data-type"></a>Тип данных

**Bool** , сохраненный как **UINT32**

## <a name="remarks"></a>Комментарии

Этот атрибут применяется только к видео МФТС. Чтобы запросить этот атрибут, вызовите [**имфтрансформ:: InAttribute**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) , чтобы получить хранилище атрибутов MFT. Если методы **InAttribute** выполнены, вызовите [**ИМФАТТРИБУТЕС:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

-   Если атрибут не равен нулю, клиент может предоставить MFT указатель на интерфейс [**имфдксгидевицеманажер**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) перед запуском потоковой передачи. Для этого клиент отправляет в основную таблицу сообщений [**MFT \_ сообщение \_ \_ \_ диспетчера D3D**](mft-message-set-d3d-manager.md) . Клиенту не требуется отсылать это сообщение.
-   Если этот атрибут равен нулю (**false**), то MFT не поддерживает Direct3D 11, и клиент не должен отсылать сообщение [**MFT \_ \_ \_ \_ диспетчера D3D**](mft-message-set-d3d-manager.md) в основную таблицу файлов.

Значение этого атрибута по умолчанию равно **false**. Рассматривайте этот атрибут как доступный только для чтения. Не изменяйте значение. в MFT все изменения в значении будут игнорироваться.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Приложения UWP для классических приложений Windows 8 \|\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Приложения UWP для классических приложений Windows Server 2012 \|\]<br/>                              |
| Header<br/>                   | <dl> <dt>Мфтрансформ. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Поддержка декодирования видео Direct3D 11 в Media Foundation](supporting-direct3d-11-video-decoding-in-media-foundation.md)
</dt> </dl>

 

 




