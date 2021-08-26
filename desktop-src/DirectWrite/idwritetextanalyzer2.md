---
title: Интерфейс IDWriteTextAnalyzer2
description: Анализирует различные свойства текста для обработки сложных скриптов.
ms.assetid: 62DF6E71-F99D-47E9-A9BE-2A481A60AEDD
keywords:
- Непосредственная запись интерфейса IDWriteTextAnalyzer2
- Непосредственная запись интерфейса IDWriteTextAnalyzer2, описание
topic_type:
- apiref
api_name:
- IDWriteTextAnalyzer2
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a76d4b4b7c2ef09f82834ed2e7f40ee89d2ab80bd0595db62790f38831b86fb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075574"
---
# <a name="idwritetextanalyzer2-interface"></a>Интерфейс IDWriteTextAnalyzer2

Анализирует различные свойства текста для обработки сложных скриптов.

## <a name="members"></a>Элементы

Интерфейс **IDWriteTextAnalyzer2** наследует от [**IDWriteTextAnalyzer1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalyzer1). **IDWriteTextAnalyzer2** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **IDWriteTextAnalyzer2** содержит следующие методы.



| Метод                                                                                    | Описание                                                                             |
|:------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------|
| [**чекктипографикфеатуре**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextanalyzer2-checktypographicfeature)           | Проверяет, доступна ли типографская функция для глифа или набора глифов.<br/> |
| [**жетглифориентатионтрансформ**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextanalyzer2-getglyphorientationtransform) | Возвращает матрицу преобразования 2 для соответствующего угла для прорисовки выполнения глифа.<br/> |
| [**жеттипографикфеатурес**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextanalyzer2-gettypographicfeatures)             | Возвращает полный список функций OpenType, доступных для сценария или шрифта.<br/> |



 

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

[**IDWriteTextAnalyzer1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalyzer1)
</dt> </dl>

 

