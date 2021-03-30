---
title: Класс MDM_RemoteWipe
description: Класс MDM \_ ремотевипе позволяет выполнять удаленную очистку устройства.
ms.assetid: 8c7c8705-8694-4ce3-ba21-ca610fe1f547
keywords:
- Класс MDM_RemoteWipe
- MDM_RemoteWipe класс, описание
topic_type:
- apiref
api_name:
- MDM_RemoteWipe
- MDM_RemoteWipe.InstanceID
- MDM_RemoteWipe.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ece626fca573e34cf938105f5e59b61e0585fd3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071157"
---
# <a name="mdm_remotewipe-class"></a><span data-ttu-id="e12c6-105">\_Класс MDM ремотевипе</span><span class="sxs-lookup"><span data-stu-id="e12c6-105">MDM\_RemoteWipe class</span></span>

<span data-ttu-id="e12c6-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="e12c6-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="e12c6-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="e12c6-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="e12c6-108">Класс **MDM \_ ремотевипе** позволяет выполнять удаленную очистку устройства.</span><span class="sxs-lookup"><span data-stu-id="e12c6-108">The **MDM\_RemoteWipe** class allows a remote wipe of a device.</span></span>

<span data-ttu-id="e12c6-109">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="e12c6-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e12c6-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e12c6-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_RemoteWipe
{
  string InstanceID;
  string ParentID;
};
```

## <a name="members"></a><span data-ttu-id="e12c6-111">Члены</span><span class="sxs-lookup"><span data-stu-id="e12c6-111">Members</span></span>

<span data-ttu-id="e12c6-112">Класс **MDM \_ ремотевипе** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="e12c6-112">The **MDM\_RemoteWipe** class has these types of members:</span></span>

-   [<span data-ttu-id="e12c6-113">Методы</span><span class="sxs-lookup"><span data-stu-id="e12c6-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="e12c6-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="e12c6-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="e12c6-115">Методы</span><span class="sxs-lookup"><span data-stu-id="e12c6-115">Methods</span></span>

<span data-ttu-id="e12c6-116">Класс **MDM \_ ремотевипе** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="e12c6-116">The **MDM\_RemoteWipe** class has these methods.</span></span>



| <span data-ttu-id="e12c6-117">Метод</span><span class="sxs-lookup"><span data-stu-id="e12c6-117">Method</span></span>                                              | <span data-ttu-id="e12c6-118">Описание</span><span class="sxs-lookup"><span data-stu-id="e12c6-118">Description</span></span>                                              |
|:----------------------------------------------------|:---------------------------------------------------------|
| [<span data-ttu-id="e12c6-119">**довипемесод**</span><span class="sxs-lookup"><span data-stu-id="e12c6-119">**doWipeMethod**</span></span>](mdm-remotewipe-dowipemethod.md) | <span data-ttu-id="e12c6-120">Запускает устройство для запуска удаленной очистки.</span><span class="sxs-lookup"><span data-stu-id="e12c6-120">Triggers the device to start the remote wipe.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="e12c6-121">Свойства</span><span class="sxs-lookup"><span data-stu-id="e12c6-121">Properties</span></span>

<span data-ttu-id="e12c6-122">Класс **MDM \_ ремотевипе** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="e12c6-122">The **MDM\_RemoteWipe** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e12c6-123">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="e12c6-123">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e12c6-124">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e12c6-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e12c6-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e12c6-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e12c6-126">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e12c6-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e12c6-127">Определяет имя родительского узла.</span><span class="sxs-lookup"><span data-stu-id="e12c6-127">Identifies the name of the parent node.</span></span> <span data-ttu-id="e12c6-128">Для этого класса строка имеет значение "Ремотевипе".</span><span class="sxs-lookup"><span data-stu-id="e12c6-128">For this class, the string is "RemoteWipe".</span></span>

</dd> <dt>

<span data-ttu-id="e12c6-129">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="e12c6-129">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e12c6-130">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e12c6-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e12c6-131">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e12c6-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e12c6-132">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e12c6-132">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e12c6-133">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="e12c6-133">Describes the full path to the parent node.</span></span> <span data-ttu-id="e12c6-134">Для этого класса строка имеет значение "./вендор/мсфт/"</span><span class="sxs-lookup"><span data-stu-id="e12c6-134">For this class, the string is "./Vendor/MSFT/"</span></span>

</dd> </dl>

## <a name="example"></a><span data-ttu-id="e12c6-135">Пример</span><span class="sxs-lookup"><span data-stu-id="e12c6-135">Example</span></span>

<span data-ttu-id="e12c6-136">В следующем примере показано, как использовать Ремотевипе и вызывать Довипемесод.</span><span class="sxs-lookup"><span data-stu-id="e12c6-136">The following example demonstrates how to use the RemoteWipe and invoke the doWipeMethod.</span></span>

> [!Note]  
> <span data-ttu-id="e12c6-137">Этот пример должен выполняться с правами локального пользователя системы.</span><span class="sxs-lookup"><span data-stu-id="e12c6-137">This example must be executed under local system user.</span></span> <span data-ttu-id="e12c6-138">Для этого скачайте средство PsExec из <https://technet.microsoft.com/sysinternals/bb897553.aspx> `psexec.exe -i -s cmd.exe` командной строки с повышенными правами администратора и запустите ее.</span><span class="sxs-lookup"><span data-stu-id="e12c6-138">To do that, download the psexec tool from <https://technet.microsoft.com/sysinternals/bb897553.aspx> and run `psexec.exe -i -s cmd.exe` from an elevated admin command prompt.</span></span>

 

``` syntax
$namespaceName = "root\cimv2\mdm\dmmap"
$className = "MDM_RemoteWipe"
$methodName = "doWipeMethod"

$session = New-CimSession

$params = New-Object Microsoft.Management.Infrastructure.CimMethodParametersCollection
$param = [Microsoft.Management.Infrastructure.CimMethodParameter]::Create("param", "", "String", "In")
$params.Add($param)

try
{
    $instance = Get-CimInstance -Namespace $namespaceName -ClassName $className -Filter "ParentID='./Vendor/MSFT' and InstanceID='RemoteWipe'"
    $session.InvokeMethod($namespaceName, $instance, $methodName, $params)
}
catch [Exception]
{
    write-host $_ | out-string
}
```

## <a name="requirements"></a><span data-ttu-id="e12c6-139">Требования</span><span class="sxs-lookup"><span data-stu-id="e12c6-139">Requirements</span></span>



| <span data-ttu-id="e12c6-140">Требование</span><span class="sxs-lookup"><span data-stu-id="e12c6-140">Requirement</span></span> | <span data-ttu-id="e12c6-141">Значение</span><span class="sxs-lookup"><span data-stu-id="e12c6-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e12c6-142">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e12c6-142">Minimum supported client</span></span><br/> | <span data-ttu-id="e12c6-143">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="e12c6-143">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e12c6-144">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e12c6-144">Minimum supported server</span></span><br/> | <span data-ttu-id="e12c6-145">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="e12c6-145">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="e12c6-146">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e12c6-146">Namespace</span></span><br/>                | <span data-ttu-id="e12c6-147">Корневой \\ CIMv2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="e12c6-147">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="e12c6-148">MOF</span><span class="sxs-lookup"><span data-stu-id="e12c6-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e12c6-149"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e12c6-149"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="e12c6-150">DLL</span><span class="sxs-lookup"><span data-stu-id="e12c6-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e12c6-151"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e12c6-151"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e12c6-152">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e12c6-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e12c6-153">Использование сценариев PowerShell с WMI Bridge Provider</span><span class="sxs-lookup"><span data-stu-id="e12c6-153">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

