---
description: Хранит сведения о типах ссылок и используется интерфейсом Иитемпревиеверекст.
ms.assetid: c1d525ea-ee80-49fb-9447-20465b8f8654
title: Структура ЛИНКИНФО
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LINKINFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: de74f7aefb61f12bf85a457e4478aa76f2156410
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262940"
---
# <a name="linkinfo-structure"></a><span data-ttu-id="d39b5-103">Структура ЛИНКИНФО</span><span class="sxs-lookup"><span data-stu-id="d39b5-103">LINKINFO structure</span></span>

<span data-ttu-id="d39b5-104">\[**Линкинфо** и [**иитемпревиеверекст**](-search-iitempreviewerext.md) поддерживаются только в Windows XP и Windows Server 2003 и больше не должны использоваться.\]</span><span class="sxs-lookup"><span data-stu-id="d39b5-104">\[**LINKINFO** and [**IItemPreviewerExt**](-search-iitempreviewerext.md) are supported only on Windows XP and Windows Server 2003, and should no longer be used.\]</span></span>

<span data-ttu-id="d39b5-105">Хранит сведения о типах ссылок и используется интерфейсом [**иитемпревиеверекст**](-search-iitempreviewerext.md) .</span><span class="sxs-lookup"><span data-stu-id="d39b5-105">Stores information about link types, and is used by the [**IItemPreviewerExt**](-search-iitempreviewerext.md) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="d39b5-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d39b5-106">Syntax</span></span>


```C++
typedef struct _LINKINFO {
  LINKTYPE type;
  BSTR     bstrContentType;
  BSTR     bstrEncoding;
  BSTR     bstrFileExt;
  VARIANT  varData;
  DWORD    dwRelatedParts;
  BSTR     bstrRelatedCid;
  Long     lCodePage;
} LINKINFO;
```



## <a name="members"></a><span data-ttu-id="d39b5-107">Члены</span><span class="sxs-lookup"><span data-stu-id="d39b5-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="d39b5-108">**type**</span><span class="sxs-lookup"><span data-stu-id="d39b5-108">**type**</span></span>
</dt> <dd>

<span data-ttu-id="d39b5-109">Тип: **/с [](-search-linktype.md)**</span><span class="sxs-lookup"><span data-stu-id="d39b5-109">Type: **[**LINKTYPE**](-search-linktype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d39b5-110">Тип ссылки, указанный при обходе или индексировании [**, указанном константой**](-search-linktype.md) типа "ссылка".</span><span class="sxs-lookup"><span data-stu-id="d39b5-110">The type of link specified when crawling or indexing indicated by a [**LINKTYPE**](-search-linktype.md) constant.</span></span>

</dd> <dt>

<span data-ttu-id="d39b5-111">**бстрконтенттипе**</span><span class="sxs-lookup"><span data-stu-id="d39b5-111">**bstrContentType**</span></span>
</dt> <dd>

<span data-ttu-id="d39b5-112">Тип: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="d39b5-112">Type: **BSTR**</span></span>

</dd> <dd>

<span data-ttu-id="d39b5-113">Значение **BSTR** , указывающее тип содержимого.</span><span class="sxs-lookup"><span data-stu-id="d39b5-113">A **BSTR** value that specifies the content type.</span></span>

</dd> <dt>

<span data-ttu-id="d39b5-114">**бстренкодинг**</span><span class="sxs-lookup"><span data-stu-id="d39b5-114">**bstrEncoding**</span></span>
</dt> <dd>

<span data-ttu-id="d39b5-115">Тип: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="d39b5-115">Type: **BSTR**</span></span>

</dd> <dd>

<span data-ttu-id="d39b5-116">Атрибут EncodingStyle, указанный в файле языка описания веб-служб (WSDL).</span><span class="sxs-lookup"><span data-stu-id="d39b5-116">An EncodingStyle attribute specified in the Web Services Description Language (WSDL) file.</span></span>

</dd> <dt>

<span data-ttu-id="d39b5-117">**бстрфиликст**</span><span class="sxs-lookup"><span data-stu-id="d39b5-117">**bstrFileExt**</span></span>
</dt> <dd>

<span data-ttu-id="d39b5-118">Тип: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="d39b5-118">Type: **BSTR**</span></span>

</dd> <dd>

<span data-ttu-id="d39b5-119">Значение **BSTR** , указывающее расширение имени файла.</span><span class="sxs-lookup"><span data-stu-id="d39b5-119">A **BSTR** value that specifies the file name extension.</span></span>

</dd> <dt>

<span data-ttu-id="d39b5-120">**вардата**</span><span class="sxs-lookup"><span data-stu-id="d39b5-120">**varData**</span></span>
</dt> <dd>

<span data-ttu-id="d39b5-121">Тип: **Variant**</span><span class="sxs-lookup"><span data-stu-id="d39b5-121">Type: **VARIANT**</span></span>

</dd> <dd>

<span data-ttu-id="d39b5-122">Вариант, указывающий значение переменной.</span><span class="sxs-lookup"><span data-stu-id="d39b5-122">A variant that specifies the variable value.</span></span>

</dd> <dt>

<span data-ttu-id="d39b5-123">**дврелатедпартс**</span><span class="sxs-lookup"><span data-stu-id="d39b5-123">**dwRelatedParts**</span></span>
</dt> <dd>

<span data-ttu-id="d39b5-124">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="d39b5-124">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="d39b5-125">Значение **типа DWORD** , указывающее связанные части.</span><span class="sxs-lookup"><span data-stu-id="d39b5-125">A **DWORD** that specifies the related parts.</span></span>

</dd> <dt>

<span data-ttu-id="d39b5-126">**бстррелатедЦид**</span><span class="sxs-lookup"><span data-stu-id="d39b5-126">**bstrRelatedCid**</span></span>
</dt> <dd>

<span data-ttu-id="d39b5-127">Тип: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="d39b5-127">Type: **BSTR**</span></span>

</dd> <dd>

<span data-ttu-id="d39b5-128">Значение **BSTR** , указывающее свойство CID, десятичную строку со знаком, которая является незаполненной.</span><span class="sxs-lookup"><span data-stu-id="d39b5-128">A **BSTR** value that specifies a Cid property, a non-padded, signed decimal string.</span></span>

</dd> <dt>

<span data-ttu-id="d39b5-129">**лкодепаже**</span><span class="sxs-lookup"><span data-stu-id="d39b5-129">**lCodePage**</span></span>
</dt> <dd>

<span data-ttu-id="d39b5-130">Тип: **Long**</span><span class="sxs-lookup"><span data-stu-id="d39b5-130">Type: **Long**</span></span>

</dd> <dd>

<span data-ttu-id="d39b5-131">Кодовая страница, используемая для кодирования строки.</span><span class="sxs-lookup"><span data-stu-id="d39b5-131">The code page to use for encoding the string.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d39b5-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d39b5-132">Remarks</span></span>

<span data-ttu-id="d39b5-133">Для предварительного просмотра вложений с помощью обработчика протокола стороннего производителя на компьютерах под управлением Windows XP или Windows Server 2003 может потребоваться использовать структуру **линкинфо** и следующие API: методы [**Иитемпревиеверекст:: жетлинкедконтент**](-search-iitempreviewerext-getlinkedcontent.md) и [**иитемпревиеверекст:: жетрелатедпарт**](-search-iitempreviewerext-getrelatedpart.md) и [**перечисление**](-search-linktype.md) типов ссылок.</span><span class="sxs-lookup"><span data-stu-id="d39b5-133">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the **LINKINFO** structure, and the following APIs: the [**IItemPreviewerExt::GetLinkedContent**](-search-iitempreviewerext-getlinkedcontent.md) and [**IItemPreviewerExt::GetRelatedPart**](-search-iitempreviewerext-getrelatedpart.md) methods, and the [**LINKTYPE**](-search-linktype.md) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="d39b5-134">Требования</span><span class="sxs-lookup"><span data-stu-id="d39b5-134">Requirements</span></span>



| <span data-ttu-id="d39b5-135">Требование</span><span class="sxs-lookup"><span data-stu-id="d39b5-135">Requirement</span></span> | <span data-ttu-id="d39b5-136">Значение</span><span class="sxs-lookup"><span data-stu-id="d39b5-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d39b5-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d39b5-137">Minimum supported client</span></span><br/> | <span data-ttu-id="d39b5-138">Только для настольных приложений Windows XP с пакетом обновления 2 \[\]</span><span class="sxs-lookup"><span data-stu-id="d39b5-138">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="d39b5-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d39b5-139">Minimum supported server</span></span><br/> | <span data-ttu-id="d39b5-140">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d39b5-140">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="d39b5-141">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="d39b5-141">Redistributable</span></span><br/>          | <span data-ttu-id="d39b5-142">Поиск на рабочем столе Windows (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="d39b5-142">Windows Desktop Search (WDS) 3.0</span></span><br/>          |



 

 




