---
title: Сообщение TB_MAPACCELERATOR (Коммктрл. h)
description: Определяет идентификатор кнопки, соответствующей указанному символу ускорителя.
ms.assetid: 724b593d-39af-4301-b721-0332844677b1
keywords:
- Элементы управления Windows для TB_MAPACCELERATOR сообщений
topic_type:
- apiref
api_name:
- TB_MAPACCELERATOR
- TB_MAPACCELERATORA
- TB_MAPACCELERATORW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 029584d9e1614a3a135da5ebd3f4f446795fd9ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803143"
---
# <a name="tb_mapaccelerator-message"></a>\_Сообщение МАПАКЦЕЛЕРАТОР ТБ

Определяет идентификатор кнопки, соответствующей указанному символу ускорителя.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* \[ окне\]
</dt> <dd>

Символ ускорителя.

</dd> <dt>

*lParam* \[ заполняет\]
</dt> <dd>

Указатель на **uint**. При возвращении в случае успеха этот параметр будет содержать идентификатор кнопки, имеющей *wParam* в качестве символа ускорителя.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Функция возвращает ненулевое значение, если одна из кнопок имеет параметр *wParam* в качестве символа ускорителя, или ноль в противном случае.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **ТБ \_ МАПАКЦЕЛЕРАТОРВ** (Юникод) и **ТБ \_ мапакцелератора** (ANSI)<br/>       |



 

 





