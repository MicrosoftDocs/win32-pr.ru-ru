---
description: Предоставляет сведения о сетевом подключении для виртуальной машины.
ms.assetid: 59503c1b-203b-46ec-8a65-f21a746f170f
title: Класс Msvm_NetworkConnectionDiagnosticInformation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_NetworkConnectionDiagnosticInformation
- Msvm_NetworkConnectionDiagnosticInformation.RoundTripTime
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 416392702e5bc06e54fe5a23b6784b87e98b7027
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999474"
---
# <a name="msvm_networkconnectiondiagnosticinformation-class"></a><span data-ttu-id="f4012-103">\_Класс мсвм нетворкконнектиондиагностиЦинформатион</span><span class="sxs-lookup"><span data-stu-id="f4012-103">Msvm\_NetworkConnectionDiagnosticInformation class</span></span>

<span data-ttu-id="f4012-104">Предоставляет сведения о сетевом подключении для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f4012-104">Provides information about the network connectivity for a virtual machine.</span></span>

<span data-ttu-id="f4012-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="f4012-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4012-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f4012-106">Syntax</span></span>

``` syntax
[AMENDMENT]
class Msvm_NetworkConnectionDiagnosticInformation
{
  uint32 RoundTripTime;
};
```

## <a name="members"></a><span data-ttu-id="f4012-107">Члены</span><span class="sxs-lookup"><span data-stu-id="f4012-107">Members</span></span>

<span data-ttu-id="f4012-108">Класс **мсвм \_ нетворкконнектиондиагностиЦинформатион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="f4012-108">The **Msvm\_NetworkConnectionDiagnosticInformation** class has these types of members:</span></span>

-   [<span data-ttu-id="f4012-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="f4012-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f4012-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="f4012-110">Properties</span></span>

<span data-ttu-id="f4012-111">Класс **мсвм \_ нетворкконнектиондиагностиЦинформатион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="f4012-111">The **Msvm\_NetworkConnectionDiagnosticInformation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f4012-112">**раундтриптиме**</span><span class="sxs-lookup"><span data-stu-id="f4012-112">**RoundTripTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4012-113">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f4012-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f4012-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f4012-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f4012-115">Время кругового пути для запроса проверки связи.</span><span class="sxs-lookup"><span data-stu-id="f4012-115">The round trip time for the ping request.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f4012-116">Требования</span><span class="sxs-lookup"><span data-stu-id="f4012-116">Requirements</span></span>



| <span data-ttu-id="f4012-117">Требование</span><span class="sxs-lookup"><span data-stu-id="f4012-117">Requirement</span></span> | <span data-ttu-id="f4012-118">Значение</span><span class="sxs-lookup"><span data-stu-id="f4012-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4012-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f4012-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f4012-120">\[Только для настольных приложений Windows 10 версии 1703\]</span><span class="sxs-lookup"><span data-stu-id="f4012-120">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="f4012-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f4012-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f4012-122">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="f4012-122">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="f4012-123">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f4012-123">Namespace</span></span><br/>                | <span data-ttu-id="f4012-124">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="f4012-124">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="f4012-125">MOF</span><span class="sxs-lookup"><span data-stu-id="f4012-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f4012-126"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f4012-126"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f4012-127">DLL</span><span class="sxs-lookup"><span data-stu-id="f4012-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f4012-128"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f4012-128"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

 




