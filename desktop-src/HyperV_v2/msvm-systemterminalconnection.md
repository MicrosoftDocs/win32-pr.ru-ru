---
description: Связывает виртуальную машину с терминальным подключением.
ms.assetid: 31979FB8-3870-44D9-9720-AD99237C5268
title: Класс Msvm_SystemTerminalConnection
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SystemTerminalConnection
- Msvm_SystemTerminalConnection.Antecedent
- Msvm_SystemTerminalConnection.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 368c25b8505ec7ddd29da3b95d95fc842602119e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682510"
---
# <a name="msvm_systemterminalconnection-class"></a><span data-ttu-id="bb984-103">\_Класс мсвм системтерминалконнектион</span><span class="sxs-lookup"><span data-stu-id="bb984-103">Msvm\_SystemTerminalConnection class</span></span>

<span data-ttu-id="bb984-104">Связывает виртуальную машину с терминальным подключением.</span><span class="sxs-lookup"><span data-stu-id="bb984-104">Associates a virtual machine with a terminal connection.</span></span>

<span data-ttu-id="bb984-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="bb984-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb984-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bb984-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SystemTerminalConnection : CIM_HostedDependency
{
  Msvm_ComputerSystem     REF Antecedent;
  Msvm_TerminalConnection REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="bb984-107">Члены</span><span class="sxs-lookup"><span data-stu-id="bb984-107">Members</span></span>

<span data-ttu-id="bb984-108">Класс **мсвм \_ системтерминалконнектион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="bb984-108">The **Msvm\_SystemTerminalConnection** class has these types of members:</span></span>

-   [<span data-ttu-id="bb984-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="bb984-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bb984-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="bb984-110">Properties</span></span>

<span data-ttu-id="bb984-111">Класс **мсвм \_ системтерминалконнектион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="bb984-111">The **Msvm\_SystemTerminalConnection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bb984-112">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="bb984-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb984-113">Тип данных: **[ **мсвм \_ ComputerSystem**](msvm-computersystem.md)**</span><span class="sxs-lookup"><span data-stu-id="bb984-113">Data type: **[**Msvm\_ComputerSystem**](msvm-computersystem.md)**</span></span>
</dt> <dt>

<span data-ttu-id="bb984-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bb984-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bb984-115">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="bb984-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="bb984-116">Виртуальная машина, к которой подключено подключение.</span><span class="sxs-lookup"><span data-stu-id="bb984-116">The virtual machine to which the connection is attached.</span></span>

</dd> <dt>

<span data-ttu-id="bb984-117">**Него**</span><span class="sxs-lookup"><span data-stu-id="bb984-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb984-118">Тип данных: **[ **мсвм \_ терминалконнектион**](msvm-terminalconnection.md)**</span><span class="sxs-lookup"><span data-stu-id="bb984-118">Data type: **[**Msvm\_TerminalConnection**](msvm-terminalconnection.md)**</span></span>
</dt> <dt>

<span data-ttu-id="bb984-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bb984-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bb984-120">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")</span><span class="sxs-lookup"><span data-stu-id="bb984-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="bb984-121">Подключение к виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="bb984-121">The connection to the virtual machine.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bb984-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bb984-122">Remarks</span></span>

<span data-ttu-id="bb984-123">Доступ к классу **\_ системтерминалконнектион мсвм** может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="bb984-123">Access to the **Msvm\_SystemTerminalConnection** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="bb984-124">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="bb984-124">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="bb984-125">Требования</span><span class="sxs-lookup"><span data-stu-id="bb984-125">Requirements</span></span>



| <span data-ttu-id="bb984-126">Требование</span><span class="sxs-lookup"><span data-stu-id="bb984-126">Requirement</span></span> | <span data-ttu-id="bb984-127">Значение</span><span class="sxs-lookup"><span data-stu-id="bb984-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb984-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bb984-128">Minimum supported client</span></span><br/> | <span data-ttu-id="bb984-129">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="bb984-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="bb984-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bb984-130">Minimum supported server</span></span><br/> | <span data-ttu-id="bb984-131">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="bb984-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bb984-132">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="bb984-132">Namespace</span></span><br/>                | <span data-ttu-id="bb984-133">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="bb984-133">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="bb984-134">MOF</span><span class="sxs-lookup"><span data-stu-id="bb984-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bb984-135"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bb984-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="bb984-136">DLL</span><span class="sxs-lookup"><span data-stu-id="bb984-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bb984-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="bb984-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="bb984-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bb984-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb984-139">**\_ХОСТЕДДЕПЕНДЕНЦИ CIM**</span><span class="sxs-lookup"><span data-stu-id="bb984-139">**CIM\_HostedDependency**</span></span>](cim-hosteddependency.md)
</dt> <dt>

<span data-ttu-id="bb984-140">[**\_ХОСТЕДДЕПЕНДЕНЦИ CIM**](/previous-versions//cc136861(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="bb984-140">[**CIM\_HostedDependency**](/previous-versions//cc136861(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="bb984-141">Классы видео</span><span class="sxs-lookup"><span data-stu-id="bb984-141">Video Classes</span></span>](video-classes.md)
</dt> </dl>

 

