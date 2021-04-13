---
title: Сообщение EM_GETIMECOMPMODE (RichEdit. h)
description: Извлекает текущий режим редактора метода ввода (IME) для элемента управления расширенного редактирования.
ms.assetid: dac96833-4c3d-4da7-9ea4-52204434ec10
keywords:
- Элементы управления Windows для EM_GETIMECOMPMODE сообщений
topic_type:
- apiref
api_name:
- EM_GETIMECOMPMODE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1feb2f5f31831e0e292bf002f24ca4978f25753a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491805"
---
# <a name="em_getimecompmode-message"></a>\_Сообщение ЖЕТИМЕКОМПМОДЕ EM

Извлекает текущий режим редактора метода ввода (IME) для элемента управления расширенного редактирования.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Не используется; должно быть равно нулю.

</dd> <dt>

*lParam* 
</dt> <dd>

Не используется; должно быть равно нулю.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение является одним из следующих значений.



| Код возврата                                                                                     | Описание                  |
|-------------------------------------------------------------------------------------------------|------------------------------|
| <dl> <dt>**ICM \_ нотопен**</dt> </dl>     | Редактор IME не открыт.<br/>  |
| <dl> <dt>**ICM \_ LEVEL3**</dt> </dl>      | Истинный встроенный режим.<br/> |
| <dl> <dt>**ICM \_ level2**</dt> </dl>      | Уровень 2.<br/>          |
| <dl> <dt>**ICM \_ level2 \_ 5**</dt> </dl>   | Уровень 2,5<br/>         |
| <dl> <dt>**ICM \_ level2 \_ СУИ**</dt> </dl> | Специальный пользовательский интерфейс.<br/>       |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



 

 





