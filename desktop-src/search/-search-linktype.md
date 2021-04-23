---
description: Указывает тип ссылки при обходе или индексировании.
ms.assetid: 2a0ddb31-df35-4da5-9950-b091cd461556
title: Перечисление типов ссылок
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LINKTYPE
api_type:
- NA
api_location: ''
ms.openlocfilehash: e5b2105e8d56a9c8042f341ffc3f24a4d7995f4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701396"
---
# <a name="linktype-enumeration"></a><span data-ttu-id="49a16-103">Перечисление типов ссылок</span><span class="sxs-lookup"><span data-stu-id="49a16-103">LINKTYPE enumeration</span></span>

<span data-ttu-id="49a16-104">\[**Перечисление** типов ссылок поддерживается только в Windows XP и windows Server 2003 и больше не должно использоваться.\]</span><span class="sxs-lookup"><span data-stu-id="49a16-104">\[The **LINKTYPE** enumeration is supported only on Windows XP and Windows Server 2003, and should no longer be used.\]</span></span>

<span data-ttu-id="49a16-105">Указывает тип ссылки при обходе или индексировании.</span><span class="sxs-lookup"><span data-stu-id="49a16-105">Specifies the type of link when crawling or indexing.</span></span>

## <a name="syntax"></a><span data-ttu-id="49a16-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="49a16-106">Syntax</span></span>


```C++
typedef enum _LINKTYPE { 
  LINKTYPE_URL      = 0x00000000,
  LINKTYPE_CONTENT  = 0x00000001,
  LINKTYPE_RELATED  = 0x00000002
} LINKTYPE;
```



## <a name="constants"></a><span data-ttu-id="49a16-107">Константы</span><span class="sxs-lookup"><span data-stu-id="49a16-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="49a16-108"><span id="LINKTYPE_URL"></span><span id="linktype_url"></span>**\_URL-адрес ссылок**</span><span class="sxs-lookup"><span data-stu-id="49a16-108"><span id="LINKTYPE_URL"></span><span id="linktype_url"></span>**LINKTYPE\_URL**</span></span>
</dt> <dd>

<span data-ttu-id="49a16-109">Указывает, следует ли индексировать тип ссылки URL-адресов.</span><span class="sxs-lookup"><span data-stu-id="49a16-109">Specifies whether the URLs link type should be indexed.</span></span>

</dd> <dt>

<span data-ttu-id="49a16-110"><span id="LINKTYPE_CONTENT"></span><span id="linktype_content"></span>**\_содержимое ссылок**</span><span class="sxs-lookup"><span data-stu-id="49a16-110"><span id="LINKTYPE_CONTENT"></span><span id="linktype_content"></span>**LINKTYPE\_CONTENT**</span></span>
</dt> <dd>

<span data-ttu-id="49a16-111">Указывает, следует ли индексировать содержимое ссылки.</span><span class="sxs-lookup"><span data-stu-id="49a16-111">Specifies whether the link content should be indexed.</span></span>

</dd> <dt>

<span data-ttu-id="49a16-112"><span id="LINKTYPE_RELATED"></span><span id="linktype_related"></span>**\_с/с**</span><span class="sxs-lookup"><span data-stu-id="49a16-112"><span id="LINKTYPE_RELATED"></span><span id="linktype_related"></span>**LINKTYPE\_RELATED**</span></span>
</dt> <dd>

<span data-ttu-id="49a16-113">Указывает связанную ссылку.</span><span class="sxs-lookup"><span data-stu-id="49a16-113">Specifies a related link.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="49a16-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="49a16-114">Remarks</span></span>

<span data-ttu-id="49a16-115">Для предварительного просмотра вложений с помощью обработчика протоколов стороннего производителя на компьютерах под управлением Windows XP или Windows Server 2003 может потребоваться **использовать флаги** [**Иитемпревиеверекст:: жетлинкедконтент**](-search-iitempreviewerext-getlinkedcontent.md) и [**иитемпревиеверекст:: жетрелатедпарт**](-search-iitempreviewerext-getrelatedpart.md) и структуру [**линкинфо**](-search-linkinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="49a16-115">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the **LINKTYPE** flags, and the following other APIs: the [**IItemPreviewerExt::GetLinkedContent**](-search-iitempreviewerext-getlinkedcontent.md) and [**IItemPreviewerExt::GetRelatedPart**](-search-iitempreviewerext-getrelatedpart.md) methods, and the [**LINKINFO**](-search-linkinfo.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="49a16-116">Требования</span><span class="sxs-lookup"><span data-stu-id="49a16-116">Requirements</span></span>



| <span data-ttu-id="49a16-117">Требование</span><span class="sxs-lookup"><span data-stu-id="49a16-117">Requirement</span></span> | <span data-ttu-id="49a16-118">Значение</span><span class="sxs-lookup"><span data-stu-id="49a16-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="49a16-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="49a16-119">Minimum supported client</span></span><br/> | <span data-ttu-id="49a16-120">Только для настольных приложений Windows XP с пакетом обновления 2 \[\]</span><span class="sxs-lookup"><span data-stu-id="49a16-120">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="49a16-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="49a16-121">Minimum supported server</span></span><br/> | <span data-ttu-id="49a16-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="49a16-122">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



 

 




