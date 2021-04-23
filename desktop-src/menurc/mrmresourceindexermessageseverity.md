---
title: Перечисление Мрмресаурцеиндексермессажесеверити (Мрмресаурцеиндексер. h)
description: Определяет константы, указывающие серьезность сообщения индексатора ресурса. Дополнительные сведения и пошаговые руководства по использованию этих API см. в разделе пакетные API индексирования ресурсов (PRI) и пользовательские системы сборки.
ms.assetid: A4734256-94BD-43BE-B93C-55B98DF8A9BF
keywords:
- Меню перечисления Мрмресаурцеиндексермессажесеверити и другие ресурсы
topic_type:
- apiref
api_name:
- MrmResourceIndexerMessageSeverity
api_location:
- MrmResourceIndexer.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fdcbb42291ab88e91eca6c16c0a6c95c3e89fd7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105661843"
---
# <a name="mrmresourceindexermessageseverity-enumeration"></a><span data-ttu-id="e95e7-105">Перечисление Мрмресаурцеиндексермессажесеверити</span><span class="sxs-lookup"><span data-stu-id="e95e7-105">MrmResourceIndexerMessageSeverity enumeration</span></span>

<span data-ttu-id="e95e7-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="e95e7-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="e95e7-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="e95e7-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="e95e7-108">Определяет константы, указывающие серьезность сообщения индексатора ресурса.</span><span class="sxs-lookup"><span data-stu-id="e95e7-108">Defines constants that specify the severity of an resource indexer message.</span></span> <span data-ttu-id="e95e7-109">Дополнительные сведения и пошаговые руководства по использованию этих API см. в разделе [пакетные API индексирования ресурсов (PRI) и пользовательские системы сборки](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="e95e7-109">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="e95e7-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e95e7-110">Syntax</span></span>


```C++
typedef enum _MrmResourceIndexerMessageSeverity { 
  MrmResourceIndexerMessageSeverityVerbose  = 1,
  MrmResourceIndexerMessageSeverityInfo     = 2,
  MrmResourceIndexerMessageSeverityWarning  = 3,
  MrmResourceIndexerMessageSeverityError    = 4
} MrmResourceIndexerMessageSeverity;
```



## <a name="constants"></a><span data-ttu-id="e95e7-111">Константы</span><span class="sxs-lookup"><span data-stu-id="e95e7-111">Constants</span></span>

<dl> <dt>

<span data-ttu-id="e95e7-112"><span id="MrmResourceIndexerMessageSeverityVerbose"></span><span id="mrmresourceindexermessageseverityverbose"></span><span id="MRMRESOURCEINDEXERMESSAGESEVERITYVERBOSE"></span>**мрмресаурцеиндексермессажесеверитивербосе**</span><span class="sxs-lookup"><span data-stu-id="e95e7-112"><span id="MrmResourceIndexerMessageSeverityVerbose"></span><span id="mrmresourceindexermessageseverityverbose"></span><span id="MRMRESOURCEINDEXERMESSAGESEVERITYVERBOSE"></span>**MrmResourceIndexerMessageSeverityVerbose**</span></span>
</dt> <dd>

<span data-ttu-id="e95e7-113">Указывает, что сообщение является подробным.</span><span class="sxs-lookup"><span data-stu-id="e95e7-113">Indicates that the message is verbose.</span></span>

</dd> <dt>

<span data-ttu-id="e95e7-114"><span id="MrmResourceIndexerMessageSeverityInfo"></span><span id="mrmresourceindexermessageseverityinfo"></span><span id="MRMRESOURCEINDEXERMESSAGESEVERITYINFO"></span>**мрмресаурцеиндексермессажесеверитинфо**</span><span class="sxs-lookup"><span data-stu-id="e95e7-114"><span id="MrmResourceIndexerMessageSeverityInfo"></span><span id="mrmresourceindexermessageseverityinfo"></span><span id="MRMRESOURCEINDEXERMESSAGESEVERITYINFO"></span>**MrmResourceIndexerMessageSeverityInfo**</span></span>
</dt> <dd>

<span data-ttu-id="e95e7-115">Указывает, что сообщение является информационным.</span><span class="sxs-lookup"><span data-stu-id="e95e7-115">Indicates that the message is informational.</span></span>

</dd> <dt>

<span data-ttu-id="e95e7-116"><span id="MrmResourceIndexerMessageSeverityWarning"></span><span id="mrmresourceindexermessageseveritywarning"></span><span id="MRMRESOURCEINDEXERMESSAGESEVERITYWARNING"></span>**мрмресаурцеиндексермессажесеверитиварнинг**</span><span class="sxs-lookup"><span data-stu-id="e95e7-116"><span id="MrmResourceIndexerMessageSeverityWarning"></span><span id="mrmresourceindexermessageseveritywarning"></span><span id="MRMRESOURCEINDEXERMESSAGESEVERITYWARNING"></span>**MrmResourceIndexerMessageSeverityWarning**</span></span>
</dt> <dd>

<span data-ttu-id="e95e7-117">Указывает, что сообщение является предупреждением.</span><span class="sxs-lookup"><span data-stu-id="e95e7-117">Indicates that the message is a warning.</span></span>

</dd> <dt>

<span data-ttu-id="e95e7-118"><span id="MrmResourceIndexerMessageSeverityError"></span><span id="mrmresourceindexermessageseverityerror"></span><span id="MRMRESOURCEINDEXERMESSAGESEVERITYERROR"></span>**мрмресаурцеиндексермессажесеверитеррор**</span><span class="sxs-lookup"><span data-stu-id="e95e7-118"><span id="MrmResourceIndexerMessageSeverityError"></span><span id="mrmresourceindexermessageseverityerror"></span><span id="MRMRESOURCEINDEXERMESSAGESEVERITYERROR"></span>**MrmResourceIndexerMessageSeverityError**</span></span>
</dt> <dd>

<span data-ttu-id="e95e7-119">Указывает, что сообщение является ошибкой.</span><span class="sxs-lookup"><span data-stu-id="e95e7-119">Indicates that the message is an error.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e95e7-120">Требования</span><span class="sxs-lookup"><span data-stu-id="e95e7-120">Requirements</span></span>



| <span data-ttu-id="e95e7-121">Требование</span><span class="sxs-lookup"><span data-stu-id="e95e7-121">Requirement</span></span> | <span data-ttu-id="e95e7-122">Значение</span><span class="sxs-lookup"><span data-stu-id="e95e7-122">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e95e7-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e95e7-123">Minimum supported client</span></span><br/> | <span data-ttu-id="e95e7-124">\[Только для настольных приложений Windows 10 версии 1803\]</span><span class="sxs-lookup"><span data-stu-id="e95e7-124">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="e95e7-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e95e7-125">Minimum supported server</span></span><br/> | <span data-ttu-id="e95e7-126">\[Только классические приложения Windows Server\]</span><span class="sxs-lookup"><span data-stu-id="e95e7-126">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="e95e7-127">Header</span><span class="sxs-lookup"><span data-stu-id="e95e7-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="e95e7-128"><dt>Мрмресаурцеиндексер. h</dt></span><span class="sxs-lookup"><span data-stu-id="e95e7-128"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e95e7-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e95e7-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e95e7-130">Интерфейсы API индексирования ресурсов пакета (PRI) и пользовательские системы сборки</span><span class="sxs-lookup"><span data-stu-id="e95e7-130">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

