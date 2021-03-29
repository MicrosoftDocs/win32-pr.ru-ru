---
title: Сообщение PSM_PAGETOINDEX (Пршт. h)
description: Принимает маркер ХПРОПШИТПАЖЕ страницы свойств и возвращает индекс, начинающийся с нуля. Это сообщение можно отправить явным образом или использовать макрос Пропшит \_ пажетоиндекс.
ms.assetid: vs|controls|~\controls\propsheet\messages\psm_pagetoindex.htm
keywords:
- Элементы управления Windows для PSM_PAGETOINDEX сообщений
topic_type:
- apiref
api_name:
- PSM_PAGETOINDEX
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13e3cb6688ab918da0dfae8affed36903e6dcea7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654542"
---
# <a name="psm_pagetoindex-message"></a>\_Сообщение ПСМ пажетоиндекс

Принимает маркер ХПРОПШИТПАЖЕ страницы свойств и возвращает индекс, начинающийся с нуля. Это сообщение можно отправить явным образом или использовать макрос [**пропшит \_ пажетоиндекс**](/windows/desktop/api/Prsht/nf-prsht-propsheet_pagetoindex) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Должен равняться нулю.

</dd> <dt>

*lParam* 
</dt> <dd>

ХПРОПШИТПАЖЕ маркер на страницу свойств.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает отсчитываемый от нуля индекс страницы вкладки свойств, указанной параметром *lParam* в случае успеха. Иначе возвращается значение -1.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                               |
| Header<br/>                   | <dl> <dt>Пршт. h</dt> </dl> |



 

 





