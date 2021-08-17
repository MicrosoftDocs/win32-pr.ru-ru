---
title: Сообщение PSM_SETTITLE (Пршт. h)
description: Задает заголовок страницы свойств. Это сообщение можно отправить явным образом или с помощью \_ макроса пропшит сеттитле.
ms.assetid: 53ce8e20-4554-41f4-bad9-fb24c2c93c34
keywords:
- элементы управления Windows сообщений PSM_SETTITLE
topic_type:
- apiref
api_name:
- PSM_SETTITLE
- PSM_SETTITLEA
- PSM_SETTITLEW
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 782d5ebf3e7fe0850b89d9f52f0dc5c406dbd41c9bdad694b41b8ae9ea4c8b0e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119985454"
---
# <a name="psm_settitle-message"></a>\_Сообщение ПСМ сеттитле

Задает заголовок страницы свойств. Это сообщение можно отправить явным образом или с помощью макроса [**пропшит \_ сеттитле**](/windows/desktop/api/Prsht/nf-prsht-propsheet_settitle) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Флаг, указывающий, включать ли префикс "Свойства" или суффикс "Properties" (в зависимости от версии) с указанной строкой заголовка. Если это значение равно КОМАНДНОМ PSH \_ проптитле, то добавляется префикс или суффикс.

</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на буфер, содержащий строку заголовка. Если [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) этого параметра имеет **значение NULL**, то страница свойств загружает строковый ресурс, указанный в параметре [**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Нет возвращаемого значения.

## <a name="remarks"></a>Remarks

В мастере Aero это сообщение можно использовать для динамического изменения заголовка внутренней страницы. Например, при обработке уведомления [PSN \_ сетактиве](psn-setactive.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                               |
| Заголовок<br/>                   | <dl> <dt>Пршт. h</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **ПСМ \_ СЕТТИТЛЕВ** (Юникод) и **ПСМ \_ сеттитлеа** (ANSI)<br/>              |



 

