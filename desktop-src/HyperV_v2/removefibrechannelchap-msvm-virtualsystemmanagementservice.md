---
description: Удаление параметров DH-CHAP (протокол проверки подлинности Диффи-Хелмана) из искусственного Fibre Channel порта виртуальной машины.
ms.assetid: f15673e2-287d-4e87-bee4-6c0f5f9178c8
title: Метод Ремовефибречаннелчап класса Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.RemoveFibreChannelChap
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 06e944c3c592b0b61ace8a72b5d42a801ab0f5df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682835"
---
# <a name="removefibrechannelchap-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="63a1c-103">Метод Ремовефибречаннелчап \_ класса Виртуалсистемманажементсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="63a1c-103">RemoveFibreChannelChap method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="63a1c-104">Удаление параметров DH-CHAP (протокол проверки подлинности Диффи-Хелмана) из искусственного Fibre Channel порта виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="63a1c-104">Removes DH-CHAP (Diffie Hellman - Challenge Handshake Authentication Protocol) parameters from a synthetic Fibre Channel port in a virtual machine.</span></span> <span data-ttu-id="63a1c-105">Этот метод завершится ошибкой, если виртуальная машина запущена.</span><span class="sxs-lookup"><span data-stu-id="63a1c-105">This method will fail if the virtual machine is running.</span></span>

## <a name="syntax"></a><span data-ttu-id="63a1c-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="63a1c-106">Syntax</span></span>


```mof
uint32 RemoveFibreChannelChap(
  [in] string FcPortSettings[]
);
```



## <a name="parameters"></a><span data-ttu-id="63a1c-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="63a1c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63a1c-108">*Фкпортсеттингс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="63a1c-108">*FcPortSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63a1c-109">Массив строк, содержащий встроенный экземпляр класса [**мсвм \_ синсетикфкпортсеттингдата**](msvm-syntheticfcportsettingdata.md) , который определяет искусственные Fibre Channel порты, из которых удаляются параметры DH-CHAP.</span><span class="sxs-lookup"><span data-stu-id="63a1c-109">An array of strings that contain an embedded instance of the [**Msvm\_SyntheticFcPortSettingData**](msvm-syntheticfcportsettingdata.md) class that define the synthetic Fibre Channel ports to remove the DH-CHAP parameters from.</span></span> <span data-ttu-id="63a1c-110">Свойство **InstanceId** каждого из этих экземпляров определяет изменяемые элементы.</span><span class="sxs-lookup"><span data-stu-id="63a1c-110">The **InstanceID** property of each of these instances identifies the elements to be modified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63a1c-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="63a1c-111">Return value</span></span>

<span data-ttu-id="63a1c-112">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="63a1c-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="63a1c-113">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="63a1c-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="63a1c-114">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="63a1c-114">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="63a1c-115">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="63a1c-115">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="63a1c-116">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="63a1c-116">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="63a1c-117">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="63a1c-117">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="63a1c-118">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="63a1c-118">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="63a1c-119">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="63a1c-119">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="63a1c-120">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="63a1c-120">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="63a1c-121">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="63a1c-121">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="63a1c-122">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="63a1c-122">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="63a1c-123">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="63a1c-123">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="63a1c-124">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="63a1c-124">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="63a1c-125">Требования</span><span class="sxs-lookup"><span data-stu-id="63a1c-125">Requirements</span></span>



| <span data-ttu-id="63a1c-126">Требование</span><span class="sxs-lookup"><span data-stu-id="63a1c-126">Requirement</span></span> | <span data-ttu-id="63a1c-127">Значение</span><span class="sxs-lookup"><span data-stu-id="63a1c-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63a1c-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="63a1c-128">Minimum supported client</span></span><br/> | <span data-ttu-id="63a1c-129">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="63a1c-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="63a1c-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="63a1c-130">Minimum supported server</span></span><br/> | <span data-ttu-id="63a1c-131">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="63a1c-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="63a1c-132">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="63a1c-132">Namespace</span></span><br/>                | <span data-ttu-id="63a1c-133">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="63a1c-133">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="63a1c-134">MOF</span><span class="sxs-lookup"><span data-stu-id="63a1c-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="63a1c-135"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="63a1c-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="63a1c-136">DLL</span><span class="sxs-lookup"><span data-stu-id="63a1c-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="63a1c-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="63a1c-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="63a1c-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="63a1c-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63a1c-139">**Мсвм \_ виртуалсистемманажементсервице**</span><span class="sxs-lookup"><span data-stu-id="63a1c-139">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




