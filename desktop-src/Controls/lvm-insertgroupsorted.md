---
title: Сообщение LVM_INSERTGROUPSORTED (Коммктрл. h)
description: Вставляет группу в упорядоченный список групп.
ms.assetid: 8ad1660b-8b64-4f02-ac1b-b7edeeea38ab
keywords:
- Элементы управления Windows для LVM_INSERTGROUPSORTED сообщений
topic_type:
- apiref
api_name:
- LVM_INSERTGROUPSORTED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 485941f803fd5af565d8b40524a9e15968e387cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892434"
---
# <a name="lvm_insertgroupsorted-message"></a>\_Сообщение LVM инсертграупсортед

Вставляет группу в упорядоченный список групп.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Указатель на структуру <a href="/windows/win32/api/commctrl/ns-commctrl-lvinsertgroupsorted">лвинсертграупсортед</a> , содержащую вставляемую группу.</dd> <dt>

*lParam* 
</dt> <dd>Должен иметь **значение NULL**.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение не используется.

## <a name="remarks"></a>Комментарии

Порядок расположения списка основан на ИДЕНТИФИКАТОРе группы. Порядок определяется определяемой приложением функцией упорядочения [**лвграупкомпаре**](/windows/win32/api/commctrl/nc-commctrl-pfnlvgroupcompare), которая передается в структуру [**лвинсертграупсортед**](/windows/win32/api/commctrl/ns-commctrl-lvinsertgroupsorted) с помощью параметра *wParam* .

> [!Note]  
> Чтобы использовать это сообщение, необходимо указать манифест, указывающий Comclt32.dll версии 6,0. Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Ссылки**
</dt> <dt>

[**лвграупкомпаре**](/windows/win32/api/commctrl/nc-commctrl-pfnlvgroupcompare)
</dt> <dt>

[**лвинсертграупсортед**](/windows/win32/api/commctrl/ns-commctrl-lvinsertgroupsorted)
</dt> </dl>

 

