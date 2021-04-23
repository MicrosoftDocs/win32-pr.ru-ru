---
description: Представляет устройство виртуальной клавиатуры.
ms.assetid: 8fe9bdd5-59e8-421d-812a-08aa3c54c88f
title: Класс Msvm_SyntheticKeyboard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticKeyboard
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 64ac153a2c20815891d8a39fd10f58562ed8d81b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650490"
---
# <a name="msvm_synthetickeyboard-class"></a><span data-ttu-id="ecc36-103">\_Класс мсвм синсетиккэйбоард</span><span class="sxs-lookup"><span data-stu-id="ecc36-103">Msvm\_SyntheticKeyboard class</span></span>

<span data-ttu-id="ecc36-104">Представляет устройство виртуальной клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="ecc36-104">Represents a synthetic keyboard device.</span></span>

<span data-ttu-id="ecc36-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="ecc36-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ecc36-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ecc36-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SyntheticKeyboard : CIM_UserDevice
{
};
```

## <a name="members"></a><span data-ttu-id="ecc36-107">Члены</span><span class="sxs-lookup"><span data-stu-id="ecc36-107">Members</span></span>

<span data-ttu-id="ecc36-108">Класс **мсвм \_ синсетиккэйбоард** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="ecc36-108">The **Msvm\_SyntheticKeyboard** class has these types of members:</span></span>

-   [<span data-ttu-id="ecc36-109">Методы</span><span class="sxs-lookup"><span data-stu-id="ecc36-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="ecc36-110">Методы</span><span class="sxs-lookup"><span data-stu-id="ecc36-110">Methods</span></span>

<span data-ttu-id="ecc36-111">Класс **мсвм \_ синсетиккэйбоард** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="ecc36-111">The **Msvm\_SyntheticKeyboard** class has these methods.</span></span>



| <span data-ttu-id="ecc36-112">Метод</span><span class="sxs-lookup"><span data-stu-id="ecc36-112">Method</span></span>                                                                  | <span data-ttu-id="ecc36-113">Описание</span><span class="sxs-lookup"><span data-stu-id="ecc36-113">Description</span></span>                         |
|:------------------------------------------------------------------------|:------------------------------------|
| [<span data-ttu-id="ecc36-114">**Равен**</span><span class="sxs-lookup"><span data-stu-id="ecc36-114">**RequestStateChange**</span></span>](msvm-synthetickeyboard-requeststatechange.md) | <span data-ttu-id="ecc36-115">Запрашивает изменение состояния.</span><span class="sxs-lookup"><span data-stu-id="ecc36-115">Requests a state change.</span></span><br/> |
| [<span data-ttu-id="ecc36-116">**Перезапуск**</span><span class="sxs-lookup"><span data-stu-id="ecc36-116">**Reset**</span></span>](msvm-synthetickeyboard-reset.md)                           | <span data-ttu-id="ecc36-117">выполняет сброс устройства.</span><span class="sxs-lookup"><span data-stu-id="ecc36-117">resets the device.</span></span><br/>       |



 

## <a name="requirements"></a><span data-ttu-id="ecc36-118">Требования</span><span class="sxs-lookup"><span data-stu-id="ecc36-118">Requirements</span></span>



| <span data-ttu-id="ecc36-119">Требование</span><span class="sxs-lookup"><span data-stu-id="ecc36-119">Requirement</span></span> | <span data-ttu-id="ecc36-120">Значение</span><span class="sxs-lookup"><span data-stu-id="ecc36-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ecc36-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ecc36-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ecc36-122">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="ecc36-122">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="ecc36-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ecc36-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ecc36-124">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="ecc36-124">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="ecc36-125">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="ecc36-125">Namespace</span></span><br/>                | <span data-ttu-id="ecc36-126">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="ecc36-126">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="ecc36-127">MOF</span><span class="sxs-lookup"><span data-stu-id="ecc36-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ecc36-128"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ecc36-128"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ecc36-129">DLL</span><span class="sxs-lookup"><span data-stu-id="ecc36-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ecc36-130"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ecc36-130"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ecc36-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ecc36-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ecc36-132">**\_УСЕРДЕВИЦЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="ecc36-132">**CIM\_UserDevice**</span></span>](cim-userdevice.md)
</dt> </dl>

 

 




