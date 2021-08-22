---
title: Интерфейс IDWriteTextLayout3
description: Представляет блок текста после полного анализа и форматирования. | Интерфейс IDWriteTextLayout3
ms.assetid: a7741740-9524-caf0-650b-56808abcf328
keywords:
- Непосредственная запись интерфейса IDWriteTextLayout3
- Непосредственная запись интерфейса IDWriteTextLayout3, описание
topic_type:
- apiref
api_name:
- IDWriteTextLayout3
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f3a6d441c3f7d8ac9bf356bd835f800e026f8c6e27cb083a57ced571ba68fe8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119070654"
---
# <a name="idwritetextlayout3-interface"></a>Интерфейс IDWriteTextLayout3

Представляет блок текста после полного анализа и форматирования.

## <a name="members"></a>Элементы

Интерфейс **IDWriteTextLayout3** наследует от [**IDWriteTextLayout2**](idwritetextlayout2.md). **IDWriteTextLayout3** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **IDWriteTextLayout3** содержит следующие методы.



| Метод                                                          | Описание                                                                                                                                                                                                                                                          |
|:----------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**жетлинеметрикс**](idwritetextlayout3-getlinemetrics.md)     | Извлекает свойства каждой строки.<br/>                                                                                                                                                                                                                        |
| [**жетлинеспаЦинг**](idwritetextlayout3-getlinespacing.md)     | Возвращает сведения о межстрочном промежутке.<br/>                                                                                                                                                                                                                            |
| [**инвалидателайаут**](idwritetextlayout3-invalidatelayout.md) | Делает макет недействительным, принудительно перемера макета перед вызовом метрик или функций рисования. Это полезно в том случае, если изменяется расположение шрифта, а макет должен быть перерисован или если размер, реализуемый клиентом, Идвритеинлинеобжект изменения. <br/> |
| [**сетлинеспаЦинг**](idwritetextlayout3-setlinespacing.md)     | Задать Междустрочный зазор.<br/>                                                                                                                                                                                                                                         |



 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8.1 \[ приложения UWP для классических приложений \|\]<br/>                                     |
| Минимальная версия сервера<br/> | Windows Server 2012 Приложения универсального \[ приложения UWP для настольных приложений \|\]<br/>                          |
| Минимальный поддерживаемый телефон<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 и среда выполнения Windows приложения\]<br/> |
| Библиотека<br/>                  | <dl> <dt>Дврите. lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[**IDWriteTextLayout2**](idwritetextlayout2.md)
</dt> </dl>

 

 





