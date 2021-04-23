---
title: Клоседкаптион. Самиланг
description: Свойство Самиланг указывает или получает язык, отображаемый для скрытых субтитров.
ms.assetid: 990fb180-cb37-4022-b236-03f5acfd3ad3
keywords:
- Проигрыватель Windows Media Клоседкаптион. Самиланг
topic_type:
- apiref
api_name:
- ClosedCaption.SAMILang
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae99b9a164e29b4adeb2fd7b23a1b79945dcb26e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694873"
---
# <a name="closedcaptionsamilang"></a><span data-ttu-id="64c93-104">Клоседкаптион. Самиланг</span><span class="sxs-lookup"><span data-stu-id="64c93-104">ClosedCaption.SAMILang</span></span>

<span data-ttu-id="64c93-105">Свойство **самиланг** указывает или получает язык, отображаемый для скрытых субтитров.</span><span class="sxs-lookup"><span data-stu-id="64c93-105">The **SAMILang** property specifies or retrieves the language displayed for closed captioning.</span></span>

``` syntax
player.closedCaption.SAMILang
```

## <a name="possible-values"></a><span data-ttu-id="64c93-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="64c93-106">Possible Values</span></span>

<span data-ttu-id="64c93-107">Это свойство является **строкой** для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="64c93-107">This property is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="64c93-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="64c93-108">Remarks</span></span>

<span data-ttu-id="64c93-109">Файл SAMI может содержать текст для одного или нескольких языков.</span><span class="sxs-lookup"><span data-stu-id="64c93-109">A SAMI file can contain text for one or many languages.</span></span> <span data-ttu-id="64c93-110">Языки, доступные для скрытых титров, определяются между тегами <STYLE> и </STYLE> в файле Sami.</span><span class="sxs-lookup"><span data-stu-id="64c93-110">The languages available for closed captioning are defined between the <STYLE> and </STYLE> tags in the SAMI file.</span></span> <span data-ttu-id="64c93-111">Идентификатор языка указывается с уникальной буквенно-цифровой строкой, которой предшествует точка (.).</span><span class="sxs-lookup"><span data-stu-id="64c93-111">A language identifier is specified with a unique alphanumeric string that is preceded by a period (.).</span></span> <span data-ttu-id="64c93-112">Имя, указанное для языка, может быть любой строкой.</span><span class="sxs-lookup"><span data-stu-id="64c93-112">The name specified for a language can be any string.</span></span> <span data-ttu-id="64c93-113">Например, для определения английского языка (США) можно использовать следующую команду:</span><span class="sxs-lookup"><span data-stu-id="64c93-113">For example, the following could be used to define US English:</span></span>


```
.ENUSCC {Name:'English Captions' lang: en-US; SAMIType:CC;}

```



<span data-ttu-id="64c93-114">Если язык SAMI не указан, по умолчанию используется первый язык, определенный в файле SAMI.</span><span class="sxs-lookup"><span data-stu-id="64c93-114">If no SAMI language is specified, the first language defined in the SAMI file is used by default.</span></span>

<span data-ttu-id="64c93-115">Значение, передаваемое с помощью *клоседкаптион*. **Самиланг** должен соответствовать атрибуту **Name** в описателе языка.</span><span class="sxs-lookup"><span data-stu-id="64c93-115">The value you pass using *ClosedCaption*.**SAMILang** must match the **Name** attribute in the language specifier.</span></span>

<span data-ttu-id="64c93-116">**Проигрыватель Windows Media 10 Mobile:** Это свойство доступно только для чтения и всегда возвращает пустую строку.</span><span class="sxs-lookup"><span data-stu-id="64c93-116">**Windows Media Player 10 Mobile:** This property is read only, and always returns an empty string.</span></span>

## <a name="examples"></a><span data-ttu-id="64c93-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="64c93-117">Examples</span></span>

<span data-ttu-id="64c93-118">В следующем примере JScript используется *клоседкаптион*. **Самиланг** в HTML-элементе SELECT для указания языка закрытого заголовка.</span><span class="sxs-lookup"><span data-stu-id="64c93-118">The following JScript example uses *ClosedCaption*.**SAMILang** in an HTML SELECT element to specify the closed caption language.</span></span> <span data-ttu-id="64c93-119">Объект **Player** создан с идентификатором "Player".</span><span class="sxs-lookup"><span data-stu-id="64c93-119">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create the SELECT element. -->
<SELECT ID = CCLANG  NAME = "CCLANG"  LANGUAGE = "JScript"

     /* Set the closed caption language when the SELECT element changes. */
        onChange = "Player.closedCaption.SAMILang = CCLANG.value;
        ">

        /* Fill in the SELECT element options. */
           <OPTION VALUE = "'Spanish Captions'">Spanish
           <OPTION VALUE = "'Japanese Captions'">Japanese
           <OPTION VALUE = "'English Captions'">English
           <OPTION VALUE = "'French Captions'">French
           <OPTION VALUE = "'German Captions'" SELECTED>German
</SELECT>

```



## <a name="requirements"></a><span data-ttu-id="64c93-120">Требования</span><span class="sxs-lookup"><span data-stu-id="64c93-120">Requirements</span></span>



| <span data-ttu-id="64c93-121">Требование</span><span class="sxs-lookup"><span data-stu-id="64c93-121">Requirement</span></span> | <span data-ttu-id="64c93-122">Значение</span><span class="sxs-lookup"><span data-stu-id="64c93-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="64c93-123">Версия</span><span class="sxs-lookup"><span data-stu-id="64c93-123">Version</span></span><br/> | <span data-ttu-id="64c93-124">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="64c93-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="64c93-125">DLL</span><span class="sxs-lookup"><span data-stu-id="64c93-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="64c93-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="64c93-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64c93-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="64c93-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64c93-128">**Добавление субтитров к цифровым носителям**</span><span class="sxs-lookup"><span data-stu-id="64c93-128">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="64c93-129">**Объект Клоседкаптион**</span><span class="sxs-lookup"><span data-stu-id="64c93-129">**ClosedCaption Object**</span></span>](closedcaption-object.md)
</dt> </dl>

 

 





