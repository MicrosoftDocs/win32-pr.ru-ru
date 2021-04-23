---
title: Перечисление Мрмдумптипе (Мрмресаурцеиндексер. h)
description: Определяет константы, указывающие тип создаваемого дампа PRI файла. Дополнительные сведения и пошаговые руководства по использованию этих API см. в разделе пакетные API индексирования ресурсов (PRI) и пользовательские системы сборки.
ms.assetid: 71E49F35-4B79-478A-A26A-C0D9A9FC2D11
keywords:
- Меню перечисления Мрмдумптипе и другие ресурсы
topic_type:
- apiref
api_name:
- MrmDumpType
api_location:
- MrmResourceIndexer.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ff693f933af299d042b97de319fb221ac133a5c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491043"
---
# <a name="mrmdumptype-enumeration"></a><span data-ttu-id="56107-105">Перечисление Мрмдумптипе</span><span class="sxs-lookup"><span data-stu-id="56107-105">MrmDumpType enumeration</span></span>

<span data-ttu-id="56107-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="56107-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="56107-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="56107-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="56107-108">Определяет константы, указывающие тип создаваемого дампа PRI файла.</span><span class="sxs-lookup"><span data-stu-id="56107-108">Defines constants that specify the type of PRI file dump to produce.</span></span> <span data-ttu-id="56107-109">Дополнительные сведения и пошаговые руководства по использованию этих API см. в разделе [пакетные API индексирования ресурсов (PRI) и пользовательские системы сборки](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="56107-109">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="56107-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="56107-110">Syntax</span></span>


```C++
typedef enum _MrmDumpType { 
  MrmDumpType_Basic     = 0,
  MrmDumpType_Detailed  = 1,
  MrmDumpType_Schema    = 2
} MrmDumpType;
```



## <a name="constants"></a><span data-ttu-id="56107-111">Константы</span><span class="sxs-lookup"><span data-stu-id="56107-111">Constants</span></span>

<dl> <dt>

<span data-ttu-id="56107-112"><span id="MrmDumpType_Basic"></span><span id="mrmdumptype_basic"></span><span id="MRMDUMPTYPE_BASIC"></span>**Мрмдумптипе \_ Basic**</span><span class="sxs-lookup"><span data-stu-id="56107-112"><span id="MrmDumpType_Basic"></span><span id="mrmdumptype_basic"></span><span id="MRMDUMPTYPE_BASIC"></span>**MrmDumpType\_Basic**</span></span>
</dt> <dd>

<span data-ttu-id="56107-113">Указывает, что дамп должен быть базовым.</span><span class="sxs-lookup"><span data-stu-id="56107-113">Specifies that the dump should be basic.</span></span>

</dd> <dt>

<span data-ttu-id="56107-114"><span id="MrmDumpType_Detailed"></span><span id="mrmdumptype_detailed"></span><span id="MRMDUMPTYPE_DETAILED"></span>**Мрмдумптипе \_ подробные сведения**</span><span class="sxs-lookup"><span data-stu-id="56107-114"><span id="MrmDumpType_Detailed"></span><span id="mrmdumptype_detailed"></span><span id="MRMDUMPTYPE_DETAILED"></span>**MrmDumpType\_Detailed**</span></span>
</dt> <dd>

<span data-ttu-id="56107-115">Указывает, что дамп должен быть подробным.</span><span class="sxs-lookup"><span data-stu-id="56107-115">Specifies that the dump should be detailed.</span></span>

</dd> <dt>

<span data-ttu-id="56107-116"><span id="MrmDumpType_Schema"></span><span id="mrmdumptype_schema"></span><span id="MRMDUMPTYPE_SCHEMA"></span>**\_Схема мрмдумптипе**</span><span class="sxs-lookup"><span data-stu-id="56107-116"><span id="MrmDumpType_Schema"></span><span id="mrmdumptype_schema"></span><span id="MRMDUMPTYPE_SCHEMA"></span>**MrmDumpType\_Schema**</span></span>
</dt> <dd>

<span data-ttu-id="56107-117">Указывает, что дамп должен быть схемой.</span><span class="sxs-lookup"><span data-stu-id="56107-117">Specifies that the dump should be a schema.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="56107-118">Требования</span><span class="sxs-lookup"><span data-stu-id="56107-118">Requirements</span></span>



| <span data-ttu-id="56107-119">Требование</span><span class="sxs-lookup"><span data-stu-id="56107-119">Requirement</span></span> | <span data-ttu-id="56107-120">Значение</span><span class="sxs-lookup"><span data-stu-id="56107-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56107-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="56107-121">Minimum supported client</span></span><br/> | <span data-ttu-id="56107-122">\[Только для настольных приложений Windows 10 версии 1803\]</span><span class="sxs-lookup"><span data-stu-id="56107-122">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="56107-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="56107-123">Minimum supported server</span></span><br/> | <span data-ttu-id="56107-124">\[Только классические приложения Windows Server\]</span><span class="sxs-lookup"><span data-stu-id="56107-124">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="56107-125">Header</span><span class="sxs-lookup"><span data-stu-id="56107-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="56107-126"><dt>Мрмресаурцеиндексер. h</dt></span><span class="sxs-lookup"><span data-stu-id="56107-126"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56107-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="56107-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56107-128">Интерфейсы API индексирования ресурсов пакета (PRI) и пользовательские системы сборки</span><span class="sxs-lookup"><span data-stu-id="56107-128">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

