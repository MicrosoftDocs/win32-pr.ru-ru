---
description: '\_Класс WMI взаимосвязей Win32 GroupUser связывает группу и учетную запись, которая является членом этой группы.'
ms.assetid: 46dd65f0-b729-4b23-8a00-bc33d1a4868b
ms.tgt_platform: multiple
title: Класс Win32_GroupUser
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_GroupUser
- Win32_GroupUser.GroupComponent
- Win32_GroupUser.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 79035ff3c56331a240704cf6605fdf72efa4e81c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496527"
---
# <a name="win32_groupuser-class"></a><span data-ttu-id="965b8-103">\_Класс Win32 GroupUser</span><span class="sxs-lookup"><span data-stu-id="965b8-103">Win32\_GroupUser class</span></span>

<span data-ttu-id="965b8-104">[Класс WMI](/windows/desktop/WmiSdk/retrieving-a-class) взаимосвязей **Win32 \_ GroupUser** связывает группу и учетную запись, которая является членом этой группы.</span><span class="sxs-lookup"><span data-stu-id="965b8-104">The **Win32\_GroupUser** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a group and an account that is a member of that group.</span></span>

<span data-ttu-id="965b8-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="965b8-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="965b8-106">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="965b8-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="965b8-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="965b8-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C508-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_GroupUser : CIM_Component
{
  Win32_Group   REF GroupComponent;
  Win32_Account REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="965b8-108">Члены</span><span class="sxs-lookup"><span data-stu-id="965b8-108">Members</span></span>

<span data-ttu-id="965b8-109">Класс **Win32 \_ GroupUser** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="965b8-109">The **Win32\_GroupUser** class has these types of members:</span></span>

-   [<span data-ttu-id="965b8-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="965b8-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="965b8-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="965b8-111">Properties</span></span>

<span data-ttu-id="965b8-112">Класс **Win32 \_ GroupUser** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="965b8-112">The **Win32\_GroupUser** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="965b8-113">**Ссылка**</span><span class="sxs-lookup"><span data-stu-id="965b8-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="965b8-114">Тип данных: **\_ Группа Win32**</span><span class="sxs-lookup"><span data-stu-id="965b8-114">Data type: **Win32\_Group**</span></span>
</dt> <dt>

<span data-ttu-id="965b8-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="965b8-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="965b8-116">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| Группа Win32 WMI \_ ")</span><span class="sxs-lookup"><span data-stu-id="965b8-116">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_Group")</span></span>
</dt> </dl>

<span data-ttu-id="965b8-117">Ссылка на экземпляр, представляющий группу, членом которой является учетная запись.</span><span class="sxs-lookup"><span data-stu-id="965b8-117">Reference to the instance representing the group of which the account is a member.</span></span>

</dd> <dt>

<span data-ttu-id="965b8-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="965b8-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="965b8-119">Тип данных: **\_ учетная запись Win32**</span><span class="sxs-lookup"><span data-stu-id="965b8-119">Data type: **Win32\_Account**</span></span>
</dt> <dt>

<span data-ttu-id="965b8-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="965b8-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="965b8-121">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| \_ учетная запись WMI Win32")</span><span class="sxs-lookup"><span data-stu-id="965b8-121">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_Account")</span></span>
</dt> </dl>

<span data-ttu-id="965b8-122">Ссылка на экземпляр, представляющий пользовательскую или системную учетную запись, которая является частью группы учетных записей.</span><span class="sxs-lookup"><span data-stu-id="965b8-122">Reference to the instance representing the user or system account that is a part of a group of accounts.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="965b8-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="965b8-123">Remarks</span></span>

<span data-ttu-id="965b8-124">Класс **Win32 \_ GroupUser** является производным от [**\_ компонента CIM**](cim-component.md).</span><span class="sxs-lookup"><span data-stu-id="965b8-124">The **Win32\_GroupUser** class is derived from [**CIM\_Component**](cim-component.md).</span></span>

## <a name="examples"></a><span data-ttu-id="965b8-125">Примеры</span><span class="sxs-lookup"><span data-stu-id="965b8-125">Examples</span></span>

<span data-ttu-id="965b8-126">Пример PowerShell с использованием Win32 \_ GroupUser для получения списка членов локальной группы см. в разделе [список членов локальной группы на удаленном компьютере с помощью WMI и примера PowerShell](https://Gallery.TechNet.Microsoft.Com/List-local-group-members-762b48c5) в коллекции TechNet.</span><span class="sxs-lookup"><span data-stu-id="965b8-126">For a PowerShell example of using Win32\_GroupUser to retrieve a list of local group members, see the [List local group members on a remote computer using WMI and PowerShell sample](https://Gallery.TechNet.Microsoft.Com/List-local-group-members-762b48c5) on TechNet Gallery.</span></span>

<span data-ttu-id="965b8-127">Пример кода VBScript для надстройки [инструментария WMI](https://Gallery.TechNet.Microsoft.Com/e493376c-1286-456b-bd4b-4ac3b0e9bb45) в коллекции TechNet использует класс **Win32 \_ GroupUser** для получения сведений о пользователях из нескольких удаленных компьютеров.</span><span class="sxs-lookup"><span data-stu-id="965b8-127">The [WMI Information Retriever](https://Gallery.TechNet.Microsoft.Com/e493376c-1286-456b-bd4b-4ac3b0e9bb45) VBScript code example on the TechNet Gallery uses the **Win32\_GroupUser** class to retrieve user information from a number of remote computers.</span></span>

## <a name="requirements"></a><span data-ttu-id="965b8-128">Требования</span><span class="sxs-lookup"><span data-stu-id="965b8-128">Requirements</span></span>



| <span data-ttu-id="965b8-129">Требование</span><span class="sxs-lookup"><span data-stu-id="965b8-129">Requirement</span></span> | <span data-ttu-id="965b8-130">Значение</span><span class="sxs-lookup"><span data-stu-id="965b8-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="965b8-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="965b8-131">Minimum supported client</span></span><br/> | <span data-ttu-id="965b8-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="965b8-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="965b8-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="965b8-133">Minimum supported server</span></span><br/> | <span data-ttu-id="965b8-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="965b8-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="965b8-135">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="965b8-135">Namespace</span></span><br/>                | <span data-ttu-id="965b8-136">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="965b8-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="965b8-137">MOF</span><span class="sxs-lookup"><span data-stu-id="965b8-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="965b8-138"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="965b8-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="965b8-139">DLL</span><span class="sxs-lookup"><span data-stu-id="965b8-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="965b8-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="965b8-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="965b8-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="965b8-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="965b8-142">**\_Компонент CIM**</span><span class="sxs-lookup"><span data-stu-id="965b8-142">**CIM\_Component**</span></span>](cim-component.md)
</dt> <dt>

<span data-ttu-id="965b8-143">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="965b8-143">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

