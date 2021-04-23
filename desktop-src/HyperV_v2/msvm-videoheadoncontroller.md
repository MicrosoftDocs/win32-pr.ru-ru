---
description: Связывает головной диск с видеоконтроллером, который его содержит.
ms.assetid: D072DF7C-D55B-4203-9FE5-B395D1EC1632
title: Класс Msvm_VideoHeadOnController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VideoHeadOnController
- Msvm_VideoHeadOnController.Antecedent
- Msvm_VideoHeadOnController.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 11065c7b7a9e23b786697c3d4f0dbd63e67d6b17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156366"
---
# <a name="msvm_videoheadoncontroller-class"></a><span data-ttu-id="7cf9d-103">\_Класс мсвм видеохеадонконтроллер</span><span class="sxs-lookup"><span data-stu-id="7cf9d-103">Msvm\_VideoHeadOnController class</span></span>

<span data-ttu-id="7cf9d-104">Связывает головной диск с видеоконтроллером, который его содержит.</span><span class="sxs-lookup"><span data-stu-id="7cf9d-104">Associates a video head with the video controller that includes it.</span></span>

<span data-ttu-id="7cf9d-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="7cf9d-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7cf9d-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7cf9d-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VideoHeadOnController : CIM_VideoHeadOnController
{
  CIM_DisplayController REF Antecedent;
  Msvm_VideoHead        REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="7cf9d-107">Члены</span><span class="sxs-lookup"><span data-stu-id="7cf9d-107">Members</span></span>

<span data-ttu-id="7cf9d-108">Класс **мсвм \_ видеохеадонконтроллер** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="7cf9d-108">The **Msvm\_VideoHeadOnController** class has these types of members:</span></span>

-   [<span data-ttu-id="7cf9d-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="7cf9d-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7cf9d-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="7cf9d-110">Properties</span></span>

<span data-ttu-id="7cf9d-111">Класс **мсвм \_ видеохеадонконтроллер** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="7cf9d-111">The **Msvm\_VideoHeadOnController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7cf9d-112">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="7cf9d-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7cf9d-113">Тип данных: **[ **CIM \_ дисплайконтроллер**](/previous-versions//cc136810(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="7cf9d-113">Data type: **[**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85))**</span></span>
</dt> <dt>

<span data-ttu-id="7cf9d-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7cf9d-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7cf9d-115">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="7cf9d-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="7cf9d-116">Видеоконтроллер, содержащий головной диск.</span><span class="sxs-lookup"><span data-stu-id="7cf9d-116">The video controller that includes the head.</span></span>

</dd> <dt>

<span data-ttu-id="7cf9d-117">**Него**</span><span class="sxs-lookup"><span data-stu-id="7cf9d-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7cf9d-118">Тип данных: **[ **мсвм \_ видеохеад**](msvm-videohead.md)**</span><span class="sxs-lookup"><span data-stu-id="7cf9d-118">Data type: **[**Msvm\_VideoHead**](msvm-videohead.md)**</span></span>
</dt> <dt>

<span data-ttu-id="7cf9d-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7cf9d-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7cf9d-120">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="7cf9d-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="7cf9d-121">Головное устройство видеоустройства.</span><span class="sxs-lookup"><span data-stu-id="7cf9d-121">The head on the video device.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7cf9d-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7cf9d-122">Remarks</span></span>

<span data-ttu-id="7cf9d-123">Доступ к классу **\_ видеохеадонконтроллер мсвм** может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="7cf9d-123">Access to the **Msvm\_VideoHeadOnController** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="7cf9d-124">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="7cf9d-124">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="7cf9d-125">Требования</span><span class="sxs-lookup"><span data-stu-id="7cf9d-125">Requirements</span></span>



| <span data-ttu-id="7cf9d-126">Требование</span><span class="sxs-lookup"><span data-stu-id="7cf9d-126">Requirement</span></span> | <span data-ttu-id="7cf9d-127">Значение</span><span class="sxs-lookup"><span data-stu-id="7cf9d-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7cf9d-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7cf9d-128">Minimum supported client</span></span><br/> | <span data-ttu-id="7cf9d-129">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="7cf9d-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="7cf9d-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7cf9d-130">Minimum supported server</span></span><br/> | <span data-ttu-id="7cf9d-131">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="7cf9d-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7cf9d-132">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="7cf9d-132">Namespace</span></span><br/>                | <span data-ttu-id="7cf9d-133">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="7cf9d-133">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="7cf9d-134">MOF</span><span class="sxs-lookup"><span data-stu-id="7cf9d-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7cf9d-135"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7cf9d-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7cf9d-136">DLL</span><span class="sxs-lookup"><span data-stu-id="7cf9d-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7cf9d-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7cf9d-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7cf9d-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7cf9d-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7cf9d-139">**\_ВИДЕОХЕАДОНКОНТРОЛЛЕР CIM**</span><span class="sxs-lookup"><span data-stu-id="7cf9d-139">**CIM\_VideoHeadOnController**</span></span>](cim-videoheadoncontroller.md)
</dt> <dt>

<span data-ttu-id="7cf9d-140">[**\_ВИДЕОХЕАДОНКОНТРОЛЛЕР CIM**](/previous-versions//cc136950(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7cf9d-140">[**CIM\_VideoHeadOnController**](/previous-versions//cc136950(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="7cf9d-141">Классы видео</span><span class="sxs-lookup"><span data-stu-id="7cf9d-141">Video Classes</span></span>](video-classes.md)
</dt> </dl>

 

