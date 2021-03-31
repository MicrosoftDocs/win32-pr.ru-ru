---
title: Сообщение BCM_GETIMAGELIST (Коммктрл. h)
description: Возвращает \_ структуру IMAGELIST, описывающую список изображений, назначенных элементу управления "Кнопка". Это сообщение можно отправить явным образом или воспользоваться макросом "Кнопка" \_ .
ms.assetid: 79383758-53d4-4955-b472-befd338cbec6
keywords:
- Элементы управления Windows для BCM_GETIMAGELIST сообщений
topic_type:
- apiref
api_name:
- BCM_GETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b0c28e997e23d6df63150fe2283d04be1a8c0d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490887"
---
# <a name="bcm_getimagelist-message"></a>\_Сообщение BCM ImageList

Возвращает структуру [**\_ IMAGELIST**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) , описывающую список изображений, назначенных элементу управления "Кнопка". Это сообщение можно отправить явным образом или воспользоваться макросом [**"Кнопка" \_**](/windows/desktop/api/Commctrl/nf-commctrl-button_getimagelist) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Не используется; должно быть равно нулю.

</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**\_ IMAGELIST**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) , содержащую сведения о списке изображений.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если сообщение завершается с ошибкой, возвращается **значение true**. В противном случае возвращается **значение false**.

## <a name="remarks"></a>Комментарии

> [!Note]  
> Чтобы использовать это сообщение, необходимо указать манифест, указывающий Comclt32.dll версии 6,0. Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





