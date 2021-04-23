---
title: Перечисление Мрмплатформверсион (Мрмресаурцеиндексер. h)
description: Определяет константы, указывающие версию платформы. Дополнительные сведения и пошаговые руководства по использованию этих API см. в разделе пакетные API индексирования ресурсов (PRI) и пользовательские системы сборки.
ms.assetid: 7BA30B8F-FB23-4DCA-930D-099C7F8476E9
keywords:
- Меню перечисления Мрмплатформверсион и другие ресурсы
topic_type:
- apiref
api_name:
- MrmPlatformVersion
api_location:
- MrmResourceIndexer.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8127d3e6e99d974315327cf89ae9e82add7bc628
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989298"
---
# <a name="mrmplatformversion-enumeration"></a><span data-ttu-id="cf724-105">Перечисление Мрмплатформверсион</span><span class="sxs-lookup"><span data-stu-id="cf724-105">MrmPlatformVersion enumeration</span></span>

<span data-ttu-id="cf724-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="cf724-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="cf724-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="cf724-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="cf724-108">Определяет константы, указывающие версию платформы.</span><span class="sxs-lookup"><span data-stu-id="cf724-108">Defines constants that specify a platform version.</span></span> <span data-ttu-id="cf724-109">Дополнительные сведения и пошаговые руководства по использованию этих API см. в разделе [пакетные API индексирования ресурсов (PRI) и пользовательские системы сборки](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="cf724-109">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="cf724-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cf724-110">Syntax</span></span>


```C++
typedef enum _MrmPlatformVersion { 
  MrmPlatformVersion_Default          = 0,
  MrmPlatformVersion_Windows10_0_0_0  = 0x010A0000,
  MrmPlatformVersion_Windows10_0_0_5  = 0x010A0005
} MrmPlatformVersion;
```



## <a name="constants"></a><span data-ttu-id="cf724-111">Константы</span><span class="sxs-lookup"><span data-stu-id="cf724-111">Constants</span></span>

<dl> <dt>

<span data-ttu-id="cf724-112"><span id="MrmPlatformVersion_Default"></span><span id="mrmplatformversion_default"></span><span id="MRMPLATFORMVERSION_DEFAULT"></span>**Мрмплатформверсион \_ по умолчанию**</span><span class="sxs-lookup"><span data-stu-id="cf724-112"><span id="MrmPlatformVersion_Default"></span><span id="mrmplatformversion_default"></span><span id="MRMPLATFORMVERSION_DEFAULT"></span>**MrmPlatformVersion\_Default**</span></span>
</dt> <dd>

<span data-ttu-id="cf724-113">Указывает, что версия платформы является версией по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="cf724-113">Specifies that the platform version is the default.</span></span>

</dd> <dt>

<span data-ttu-id="cf724-114"><span id="MrmPlatformVersion_Windows10_0_0_0"></span><span id="mrmplatformversion_windows10_0_0_0"></span><span id="MRMPLATFORMVERSION_WINDOWS10_0_0_0"></span>**Мрмплатформверсион \_ Windows 10 \_ 0 \_ 0 \_**</span><span class="sxs-lookup"><span data-stu-id="cf724-114"><span id="MrmPlatformVersion_Windows10_0_0_0"></span><span id="mrmplatformversion_windows10_0_0_0"></span><span id="MRMPLATFORMVERSION_WINDOWS10_0_0_0"></span>**MrmPlatformVersion\_Windows10\_0\_0\_0**</span></span>
</dt> <dd>

<span data-ttu-id="cf724-115">Указывает версию платформы Windows 10.0.0.0.</span><span class="sxs-lookup"><span data-stu-id="cf724-115">Specifies a platform version of Windows 10.0.0.0.</span></span>

</dd> <dt>

<span data-ttu-id="cf724-116"><span id="MrmPlatformVersion_Windows10_0_0_5"></span><span id="mrmplatformversion_windows10_0_0_5"></span><span id="MRMPLATFORMVERSION_WINDOWS10_0_0_5"></span>**Мрмплатформверсион \_ Windows 10 \_ 0 \_ 0 \_**</span><span class="sxs-lookup"><span data-stu-id="cf724-116"><span id="MrmPlatformVersion_Windows10_0_0_5"></span><span id="mrmplatformversion_windows10_0_0_5"></span><span id="MRMPLATFORMVERSION_WINDOWS10_0_0_5"></span>**MrmPlatformVersion\_Windows10\_0\_0\_5**</span></span>
</dt> <dd>

<span data-ttu-id="cf724-117">Указывает версию платформы Windows 10.0.0.5.</span><span class="sxs-lookup"><span data-stu-id="cf724-117">Specifies a platform version of Windows 10.0.0.5.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cf724-118">Требования</span><span class="sxs-lookup"><span data-stu-id="cf724-118">Requirements</span></span>



| <span data-ttu-id="cf724-119">Требование</span><span class="sxs-lookup"><span data-stu-id="cf724-119">Requirement</span></span> | <span data-ttu-id="cf724-120">Значение</span><span class="sxs-lookup"><span data-stu-id="cf724-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf724-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cf724-121">Minimum supported client</span></span><br/> | <span data-ttu-id="cf724-122">\[Только для настольных приложений Windows 10 версии 1803\]</span><span class="sxs-lookup"><span data-stu-id="cf724-122">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="cf724-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cf724-123">Minimum supported server</span></span><br/> | <span data-ttu-id="cf724-124">\[Только классические приложения Windows Server\]</span><span class="sxs-lookup"><span data-stu-id="cf724-124">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="cf724-125">Header</span><span class="sxs-lookup"><span data-stu-id="cf724-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf724-126"><dt>Мрмресаурцеиндексер. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf724-126"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf724-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cf724-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf724-128">Интерфейсы API индексирования ресурсов пакета (PRI) и пользовательские системы сборки</span><span class="sxs-lookup"><span data-stu-id="cf724-128">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

