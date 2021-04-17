---
title: Интерфейс IDWriteTextFormat1
description: Описывает свойства шрифта и абзаца, используемые для форматирования текста, а также сведения о языковых стандартах. | Интерфейс IDWriteTextFormat1
ms.assetid: 15295A17-E542-4071-AE38-02014A1235D5
keywords:
- Непосредственная запись интерфейса IDWriteTextFormat1
- Непосредственная запись интерфейса IDWriteTextFormat1, описание
topic_type:
- apiref
api_name:
- IDWriteTextFormat1
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 796c5f845b5ed0d0522039865f2acb023fc2ab0c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105664864"
---
# <a name="idwritetextformat1-interface"></a>Интерфейс IDWriteTextFormat1

Описывает свойства шрифта и абзаца, используемые для форматирования текста, а также сведения о языковых стандартах. Этот интерфейс имеет все те же методы, что и [**идвритетекстформат**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) , и добавляет возможность применения явной ориентации.

## <a name="members"></a>Элементы

Интерфейс **IDWriteTextFormat1** наследует от [**идвритетекстформат**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat). **IDWriteTextFormat1** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **IDWriteTextFormat1** содержит следующие методы.



| Метод                                                                                | Описание                                                                                                             |
|:--------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [**жетфонтфаллбакк**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-getfontfallback)                         | Возвращает текущий откат. Если после создания макета ни один из них не был задан, он будет иметь значение nullptr.<br/>               |
| [**жетластлиневраппинг**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-getlastlinewrapping)                 | Возвращает режим переноса для последней строки.<br/>                                                                     |
| [**жетоптикалалигнмент**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-getopticalalignment)                 | Возвращает выравнивание оптического поля для текстового формата.<br/>                                                       |
| [**жетвертикалглифориентатион**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-getverticalglyphorientation) | Получение предпочтительной ориентации глифов при использовании направления чтения по вертикали.<br/>                             |
| [**сетфонтфаллбакк**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-setfontfallback)                         | Применяет к макету пользовательский откат шрифта. Если параметр не задан, используется список резервных системных систем по умолчанию. <br/> |
| [**сетластлиневраппинг**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-setlastlinewrapping)                   | Задает режим переноса для последней строки.<br/>                                                                     |
| [**сетоптикалалигнмент**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-setopticalalignment)                 | Задает для текстового формата выравнивание в виде оптического поля.<br/>                                                       |
| [**сетвертикалглифориентатион**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-setverticalglyphorientation) | Задает ориентацию текстового формата.<br/>                                                                       |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Приложения UWP для классических приложений Windows 8.1 \|\]<br/>                                     |
| Минимальная версия сервера<br/> | \[Приложения UWP для классических приложений Windows Server 2012 R2 \|\]<br/>                          |
| Минимальный поддерживаемый телефон<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 и среда выполнения Windows приложения\]<br/> |
| Библиотека<br/>                  | <dl> <dt>Дврите. lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**идвритетекстформат**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat)
</dt> </dl>

 

