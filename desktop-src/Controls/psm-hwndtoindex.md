---
title: Сообщение PSM_HWNDTOINDEX (Пршт. h)
description: Принимает маркер окна страницы свойств и возвращает индекс, начинающийся с нуля. Это сообщение можно отправить явным образом или использовать макрос Пропшит \_ хвндтоиндекс.
ms.assetid: vs|controls|~\controls\propsheet\messages\psm_hwndtoindex.htm
keywords:
- Элементы управления Windows для PSM_HWNDTOINDEX сообщений
topic_type:
- apiref
api_name:
- PSM_HWNDTOINDEX
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6632d331a6f271e339663a23210d0b399fb669b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136243"
---
# <a name="psm_hwndtoindex-message"></a>\_Сообщение ПСМ хвндтоиндекс

Принимает маркер окна страницы свойств и возвращает индекс, начинающийся с нуля. Это сообщение можно отправить явным образом или использовать макрос [**пропшит \_ хвндтоиндекс**](/windows/desktop/api/Prsht/nf-prsht-propsheet_hwndtoindex) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Обработчик для окна страницы.

</dd> <dt>

*lParam* 
</dt> <dd>

Должен равняться нулю.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает отсчитываемый от нуля индекс страницы вкладки свойств, указанной параметром *wParam* в случае успеха. Иначе возвращается значение -1.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                               |
| Header<br/>                   | <dl> <dt>Пршт. h</dt> </dl> |



 

 





