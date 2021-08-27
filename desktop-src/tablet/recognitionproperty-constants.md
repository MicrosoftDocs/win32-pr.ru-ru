---
description: Определяет значения, указывающие свойства альтернативного распознавания. Интерфейс прикладного программирования (API) Tablet PC использует глобальные уникальные идентификаторы (GUID) для идентификации свойств пакетов, которые в автоматизации являются константными строками.
ms.assetid: 2bfb0cbf-73a3-4e83-a4e9-f0803bd3dee8
title: Константы Рекогнитионпроперти (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d06d2eed3b28ed99d180dbe3971e9e018554ff5
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467991"
---
# <a name="recognitionproperty-constants"></a>Константы Рекогнитионпроперти

Определяет значения, указывающие свойства альтернативного распознавания. Интерфейс прикладного программирования (API) Tablet PC использует глобальные уникальные идентификаторы (GUID) для идентификации свойств пакетов, которые в автоматизации являются константными строками.

В следующей таблице перечислены доступные поля для альтернативного уникального идентификатора (GUID) распознавания альтернативных свойств. Используйте эти идентификаторы GUID для доступа к свойствам объекта [**иинкрекогнитионалтернате**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate) , вызвав метод [**жетпропертивалуе**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-getpropertyvalue) .




| Имя константы | Описание | 
|---------------|-------------|
| <span id="___________INKRECOGNITIONPROPERTY_LINENUMBER_________"></span><span id="___________inkrecognitionproperty_linenumber_________"></span><dl><dt><strong>INKRECOGNITIONPROPERTY_LINENUMBER</strong></dt></dl> | Идентификатор GUID, определяющий свойство для номера строки объекта <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>иинкрекогнитионалтернате</strong></a> . <br /> Номер_строки указывает варианты с определенным номером строки.<br /><blockquote>[!Note]<br />Это поле не поддерживается для распознавателей символов восточноазиатских языков.</blockquote><br /> | 
| <span id="___________INKRECOGNITIONPROPERTY_SEGMENTATION_________"></span><span id="___________inkrecognitionproperty_segmentation_________"></span><dl><dt><strong>INKRECOGNITIONPROPERTY_SEGMENTATION</strong></dt></dl> | Идентификатор GUID, определяющий свойство для сегментации объекта <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>иинкрекогнитионалтернате</strong></a> . <br /> Сегментация указывает основной фрагмент или единицу рукописного ввода, которую распознаватель использует для получения результата распознавания.<br /><blockquote>[!Note]<br />Не реализован.</blockquote><br /> | 
| <span id="___________INKRECOGNITIONPROPERTY_HOTPOINT_________"></span><span id="___________inkrecognitionproperty_hotpoint_________"></span><dl><dt><strong>INKRECOGNITIONPROPERTY_HOTPOINT</strong></dt></dl> | Идентификатор GUID, определяющий свойство для горячей точки распознавания объекта <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>иинкрекогнитионалтернате</strong></a> . <br /> | 
| <span id="___________INKRECOGNITIONPROPERTY_MAXIMUMSTROKECOUNT_________"></span><span id="___________inkrecognitionproperty_maximumstrokecount_________"></span><dl><dt><strong>INKRECOGNITIONPROPERTY_MAXIMUMSTROKECOUNT</strong></dt></dl> | Идентификатор GUID, определяющий свойство для максимального числа штрихов для результата распознавания объекта <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>иинкрекогнитионалтернате</strong></a> . <br /><blockquote>[!Note]<br />Не реализован.</blockquote><br /> | 
| <span id="___________INKRECOGNITIONPROPERTY_POINTSPERINCH_________"></span><span id="___________inkrecognitionproperty_pointsperinch_________"></span><dl><dt><strong>INKRECOGNITIONPROPERTY_POINTSPERINCH</strong></dt></dl> | Идентификатор GUID, определяющий свойство для метрики объекта <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>иинкрекогнитионалтернате</strong></a> в точках на дюйм. <br /><blockquote>[!Note]<br />Не реализован.</blockquote><br /> | 
| <span id="___________INKRECOGNITIONPROPERTY_CONFIDENCELEVEL_________"></span><span id="___________inkrecognitionproperty_confidencelevel_________"></span><dl><dt><strong>INKRECOGNITIONPROPERTY_CONFIDENCELEVEL</strong></dt></dl> | Идентификатор GUID, определяющий свойство для уровня достоверности, который распознаватель имеет в результате распознавания.<br /><blockquote>[!Note]<br />оценка достоверности доступна только для США английского и всех распознавателей жестов в Microsoft Windows XP Tablet PC Edition и Windows Vista. Методы, которые предоставляют свойство достоверности для любого другого распознавателя, возвращающего E_NOTIMPL.</blockquote><br /> | 
| <span id="___________INKRECOGNITIONPROPERTY_LINEMETRICS_________"></span><span id="___________inkrecognitionproperty_linemetrics_________"></span><dl><dt><strong>INKRECOGNITIONPROPERTY_LINEMETRICS</strong></dt></dl> | Идентификатор GUID, определяющий свойство для метрик линии объекта <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>иинкрекогнитионалтернате</strong></a> , который является строкой, для которой извлекаются метрики. <br /> | 




## <a name="remarks"></a>Комментарии

в C++ вы можете получить доступ к этим константам в файле заголовка мсинкаут. h, который находится в папке <systemdrive> : \\ Program files \\ Microsoft sdks \\ Windows \\ v 6.0 \\ Include, если пакет SDK установлен в расположение по умолчанию.

> [!Note]  
> В C++ эти константы являются Вчарс, а не BSTRs. Преобразуйте их в BSTRs перед использованием. Дополнительные сведения о типе данных BSTR см. в разделе [Использование библиотеки COM](using-the-com-library.md).

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP Tablet PC Edition \[ только классические приложения\]<br/>                                                       |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                           |
| Заголовок<br/>                   | <dl> <dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Метод Алтернатесвисконстантпропертивалуес**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-alternateswithconstantpropertyvalues)
</dt> <dt>

[**Конфиденцеалтернатес, свойство**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-get_confidencealternates)
</dt> <dt>

[**Линеалтернатес, свойство**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-get_linealternates)
</dt> <dt>

[**Интерфейс Иинкрекогнитионалтернатес**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternates)
</dt> </dl>

 

 




