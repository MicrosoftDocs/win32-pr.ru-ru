---
description: Связывает заголовку видео с видеоадаптером, который его содержит.
ms.assetid: d15f4350-1529-4246-9ea2-8453e52516c6
title: Класс CIM_VideoHeadOnController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VideoHeadOnController
- CIM_VideoHeadOnController.Antecedent
- CIM_VideoHeadOnController.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 18178e6d9d7f1e684af1d4fe74336e1f2a02eedc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662806"
---
# <a name="cim_videoheadoncontroller-class"></a><span data-ttu-id="c4eed-103">\_Класс CIM видеохеадонконтроллер</span><span class="sxs-lookup"><span data-stu-id="c4eed-103">CIM\_VideoHeadOnController class</span></span>

<span data-ttu-id="c4eed-104">Связывает заголовку видео с видеоадаптером, который его содержит.</span><span class="sxs-lookup"><span data-stu-id="c4eed-104">Associates a video head with the video adapter that contains it.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4eed-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c4eed-105">Syntax</span></span>

``` syntax
[Association, Experimental, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Device::Controller"), AMENDMENT]
class CIM_VideoHeadOnController : CIM_HostedDependency
{
  CIM_DisplayController REF Antecedent;
  CIM_VideoHead         REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="c4eed-106">Члены</span><span class="sxs-lookup"><span data-stu-id="c4eed-106">Members</span></span>

<span data-ttu-id="c4eed-107">Класс **CIM \_ видеохеадонконтроллер** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="c4eed-107">The **CIM\_VideoHeadOnController** class has these types of members:</span></span>

-   [<span data-ttu-id="c4eed-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="c4eed-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c4eed-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="c4eed-109">Properties</span></span>

<span data-ttu-id="c4eed-110">Класс **CIM \_ видеохеадонконтроллер** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="c4eed-110">The **CIM\_VideoHeadOnController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c4eed-111">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="c4eed-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4eed-112">Тип данных: **CIM \_ дисплайконтроллер**</span><span class="sxs-lookup"><span data-stu-id="c4eed-112">Data type: **CIM\_DisplayController**</span></span>
</dt> <dt>

<span data-ttu-id="c4eed-113">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c4eed-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c4eed-114">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="c4eed-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="c4eed-115">Видеоадаптер, включающий головную карту.</span><span class="sxs-lookup"><span data-stu-id="c4eed-115">The video adapter that includes the head.</span></span>

</dd> <dt>

<span data-ttu-id="c4eed-116">**Него**</span><span class="sxs-lookup"><span data-stu-id="c4eed-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4eed-117">Тип данных: **CIM \_ видеохеад**</span><span class="sxs-lookup"><span data-stu-id="c4eed-117">Data type: **CIM\_VideoHead**</span></span>
</dt> <dt>

<span data-ttu-id="c4eed-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c4eed-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c4eed-119">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="c4eed-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="c4eed-120">Головной элемент видеоадаптера.</span><span class="sxs-lookup"><span data-stu-id="c4eed-120">The head on the video adapter.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c4eed-121">Требования</span><span class="sxs-lookup"><span data-stu-id="c4eed-121">Requirements</span></span>



| <span data-ttu-id="c4eed-122">Требование</span><span class="sxs-lookup"><span data-stu-id="c4eed-122">Requirement</span></span> | <span data-ttu-id="c4eed-123">Значение</span><span class="sxs-lookup"><span data-stu-id="c4eed-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4eed-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c4eed-124">Minimum supported client</span></span><br/> | <span data-ttu-id="c4eed-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="c4eed-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="c4eed-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c4eed-126">Minimum supported server</span></span><br/> | <span data-ttu-id="c4eed-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c4eed-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="c4eed-128">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c4eed-128">Namespace</span></span><br/>                | <span data-ttu-id="c4eed-129">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="c4eed-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="c4eed-130">MOF</span><span class="sxs-lookup"><span data-stu-id="c4eed-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c4eed-131"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c4eed-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c4eed-132">DLL</span><span class="sxs-lookup"><span data-stu-id="c4eed-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c4eed-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c4eed-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c4eed-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c4eed-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4eed-135">**\_ХОСТЕДДЕПЕНДЕНЦИ CIM**</span><span class="sxs-lookup"><span data-stu-id="c4eed-135">**CIM\_HostedDependency**</span></span>](cim-hosteddependency.md)
</dt> </dl>

 

