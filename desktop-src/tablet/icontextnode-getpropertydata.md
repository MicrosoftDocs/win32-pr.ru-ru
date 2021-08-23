---
description: Извлекает данные конкретного приложения или другие данные свойства для указанного идентификатора.
ms.assetid: eaf95ff8-7b31-4c05-aa49-0c3bb9e996c0
title: 'Метод Иконтекстноде:: Жетпропертидата (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetPropertyData
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 89e7ab9fb5213b41d53695b516b95b47193e8d803b207efd09216c743085927e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119660724"
---
# <a name="icontextnodegetpropertydata-method"></a>Метод Иконтекстноде:: Жетпропертидата

Извлекает данные конкретного приложения или другие данные свойства для указанного идентификатора.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetPropertyData(
  [in]      const GUID  *pPropertyDataId,
  [in, out]       ULONG *pulPropertyDataSize,
  [out]           BYTE  **ppbPropertyData
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппропертидатаид* \[ окне\]
</dt> <dd>

Идентификатор данных.

</dd> <dt>

*пулпропертидатасизе* \[ в, out\]
</dt> <dd>

Размер данных в байтах. Передаваемое значение не используется.

</dd> <dt>

*ппбпропертидата* \[ заполняет\]
</dt> <dd>

Указатель на 8-разрядный массив целых чисел без знака, содержащий данные свойства.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Remarks

> [!Caution]  
> Чтобы избежать утечки памяти, используйте [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) , чтобы освободить память от \* *ппбпропертидата* , если эта информация больше не нужна.

 

Помимо извлечения данных приложения, которые были добавлены с помощью [**иконтекстноде:: аддпропертидата**](icontextnode-addpropertydata.md), этот метод используется для получения общих свойств, описанных в константах [свойств узла контекста](context-node-properties.md) .

К свойствам строкового типа относятся:

-   GUID \_ КНП \_ рекогнизедстринг
-   GUID \_ КНП \_ шапенаме
-   GUID \_ ахп \_ аналисишинтнаме
-   GUID \_ ахп \_ префикстекст
-   GUID \_ ахп \_ суффикстекст
-   GUID \_ ахп \_ фактоид

Возвращаемое значение — **WCHAR \**_. При приведении параметра \_ *ппбпропертидата* к **WCHAR \**_ возвращаемая длина имеет значение `(length of the string + 1) _ sizeof(WCHAR)` .

Ниже перечислены свойства логического типа.

-   GUID \_ ахп \_ оверриделангуажеид
-   GUID \_ ахп \_ коерцетофактоид
-   GUID \_ ахп \_ вордмоде

Возвращаемое значение является **вариантным \_ bool**. При приведении параметра \* *ппбпропертидата* к типу **Variant \_ bool \*** возвращаемая длина имеет значение `sizeof(VARIANT_BOOL)` .

GUID \_ ахп \_ Guide — это свойство типа "руководство". Возвращаемое значение — **инканалисисрекогнитионгуиде \** _. При приведении параметра \_ *Ппбпропертидата* к **\* инканалисисрекогнитионгуиде** его возвращаемая длина имеет значение `sizeof(InkAnalysisRecognitionGuide)` .

Свойства целочисленного типа включают:

-   GUID \_ КНП \_ LINENUMBER
-   GUID \_ КНП \_ поинтсперинч
-   GUID \_ КНП \_ конфиденцелевел
-   \_Подтверждение GUID КНП \_
-   GUID \_ КНП \_ максимумстрокекаунт
-   \_ \_ сегментация КНП GUID
-   GUID \_ КНП \_ алигнментлевел

Возвращаемое значение — **Long \** _. При приведении параметра \_ *ппбпропертидата* к типу **Long \*** возвращаемая длина имеет значение `sizeof(LONG)` .

Метрики линий — свойства типа включают:

-   GUID \_ КНП \_ ascends
-   GUID \_ КНП \_ нижние выносные
-   Базовый идентификатор GUID \_ КНП \_
-   GUID \_ КНП \_ заполнение нажатием клавиши

Возвращаемое значение — **Long \**_. Если параметр ппбпропертидата приводится к значению \_  **Long \**_ , его возвращаемая длина равна `sizeof(LONG)_4` , что означает (x, y) начальные точки, за которыми следуют значения (x, y) для конечных точек.

GUID \_ КНП \_ текстрекогнизерид является свойством **GUID** . Возвращаемое значение — **GUID \** _. При приведении параметра \_ *Ппбпропертидата* к **идентификатору \* GUID** возвращаемой длины будет `sizeof(GUID)` .

GUID \_ КНП \_ ротатедбаундингбокс — это повернутое свойство ограничивающего прямоугольника. Возвращаемое значение — **Long \**_. Если параметр ппбпропертидата приводится к значению \_  **Long \**_ , его возвращаемая длина равна `sizeof(LONG)_8` , что означает (x, y) четырех углов бокса.

GUID \_ КНП \_ хотпоинт является свойством горячей точки. Возвращаемое значение — **Long \**_. Если параметр ппбпропертидата приводится к значению \_  **Long \**_ , его возвращаемая длина равна `sizeof(LONG)_2` , что означает (x, y) точки.

GUID \_ ахп \_ список слов — это свойство списка слов. Возвращаемое значение — **WCHAR \**_. При приведении параметра \_ *ппбпропертидата* к значению ** \* WCHAR*_ возвращаемой длины является `n _ sizeof(WCHAR)` , где `n` — сумма длины строк числа строк в списке плюс 1 для каждого завершающего символа **null** для каждой строки.

## <a name="examples"></a>Примеры

В этом примере показан метод, который обращается к свойству узла контекста Алигнментлевел типа узла контекста абзаца.


```C++
// Checks a paragraph context node's alignment level property.
// Only paragraph type context nodes contain the alignment level property.
HRESULT CMyClass::ExploreParagraphNode(
    IContextNode *pParagraphNode)
{
    // Get the AlignmentLevel property data for the paragraph.
    LONG * alignmentLevel = NULL;
    ULONG ulDataLen = 0;

    HRESULT hr = pParagraphNode->GetPropertyData(
        (const GUID*)&GUID_CNP_ALIGNMENTLEVEL,
        &ulDataLen,
        (BYTE**)&alignmentLevel);

    if( FAILED(hr) ||
        ulDataLen != sizeof(LONG) ||
        alignmentLevel == NULL )
    {
        // Insert code that handles an error here.
    }
    else
    {
        // Insert code that uses the alignment level here.
    }

    // Free the memory allocated for the property data.
    ::CoTaskMemFree(alignmentLevel);

    return hr;
}
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP Tablet PC Edition \[ только классические приложения\]<br/>                                                 |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                     |
| Заголовок<br/>                   | <dl> <dt>Иаком. h (также требуется Иаком \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>См. также

<dl> <dt>

[**иконтекстноде**](icontextnode.md)
</dt> <dt>

[**Иконтекстноде:: Аддпропертидата**](icontextnode-addpropertydata.md)
</dt> <dt>

[**Иконтекстноде:: Ремовепропертидата**](icontextnode-removepropertydata.md)
</dt> <dt>

[**Иконтекстноде:: Жетпропертидатаидс**](icontextnode-getpropertydataids.md)
</dt> <dt>

[**Иконтекстноде:: Контаинспропертидата**](icontextnode-containspropertydata.md)
</dt> <dt>

[**Иконтекстноде:: Лоадпропертиесдата**](icontextnode-loadpropertiesdata.md)
</dt> <dt>

[**Иконтекстноде:: Савепропертиесдата**](icontextnode-savepropertiesdata.md)
</dt> <dt>

[Справочник по анализу рукописного ввода](ink-analysis-reference.md)
</dt> </dl>

 

