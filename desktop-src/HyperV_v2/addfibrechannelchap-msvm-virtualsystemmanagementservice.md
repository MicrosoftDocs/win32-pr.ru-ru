---
description: Добавляет параметры DH-CHAP (протокол проверки пароля Диффи-Хелмана) в виртуальный порт Fibre Channel виртуальной машины.
ms.assetid: b9799ea4-f948-4b5c-bd18-1faa90213bb3
title: Метод Аддфибречаннелчап класса Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.AddFibreChannelChap
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 07151a902efa8f8077debc44bd732286c0a96a81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998566"
---
# <a name="addfibrechannelchap-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="6551f-103">Метод Аддфибречаннелчап \_ класса Виртуалсистемманажементсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="6551f-103">AddFibreChannelChap method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="6551f-104">Добавляет параметры DH-CHAP (протокол проверки пароля Диффи-Хелмана) в виртуальный порт Fibre Channel виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="6551f-104">Adds DH-CHAP (Diffie Hellman - Challenge Handshake Authentication Protocol) parameters to a synthetic Fibre Channel port on a virtual machine.</span></span> <span data-ttu-id="6551f-105">Этот метод завершится ошибкой, если виртуальная машина запущена.</span><span class="sxs-lookup"><span data-stu-id="6551f-105">This method will fail if the virtual machine is running.</span></span>

## <a name="syntax"></a><span data-ttu-id="6551f-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6551f-106">Syntax</span></span>


```mof
uint32 AddFibreChannelChap(
  [in] string FcPortSettings[],
  [in] uint8  SecretEncoding,
  [in] uint8  SharedSecret[]
);
```



## <a name="parameters"></a><span data-ttu-id="6551f-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="6551f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6551f-108">*Фкпортсеттингс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6551f-108">*FcPortSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6551f-109">Массив строк, содержащий встроенный экземпляр класса [**мсвм \_ синсетикфкпортсеттингдата**](msvm-syntheticfcportsettingdata.md) , который описывает параметры для портов искусственного Fibre Channel для виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="6551f-109">An array of strings that contain an embedded instance of the [**Msvm\_SyntheticFcPortSettingData**](msvm-syntheticfcportsettingdata.md) class that describes settings for synthetic Fibre Channel ports for virtual machines.</span></span> <span data-ttu-id="6551f-110">Свойство **InstanceId** каждого из этих экземпляров определяет изменяемые элементы.</span><span class="sxs-lookup"><span data-stu-id="6551f-110">The **InstanceID** property of each of these instances identifies the elements to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="6551f-111">*Секретенкодинг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6551f-111">*SecretEncoding* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6551f-112">Указывает тип кодировки для общего секрета.</span><span class="sxs-lookup"><span data-stu-id="6551f-112">Specifies the type of encoding for the shared secret.</span></span>

<dt>

<span id="Printable_ASCII"></span><span id="printable_ascii"></span><span id="PRINTABLE_ASCII"></span>

<span data-ttu-id="6551f-113">**Печатный текст ASCII** (1)</span><span class="sxs-lookup"><span data-stu-id="6551f-113">**Printable ASCII** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Binary"></span><span id="binary"></span><span id="BINARY"></span>

<span data-ttu-id="6551f-114">**Двоичный** (2)</span><span class="sxs-lookup"><span data-stu-id="6551f-114">**Binary** (2)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="6551f-115">*SharedSecret* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6551f-115">*SharedSecret* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6551f-116">Указывает общий секрет.</span><span class="sxs-lookup"><span data-stu-id="6551f-116">Specifies the shared secret.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6551f-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6551f-117">Return value</span></span>

<span data-ttu-id="6551f-118">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="6551f-118">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="6551f-119">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="6551f-119">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="6551f-120">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="6551f-120">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="6551f-121">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="6551f-121">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="6551f-122">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="6551f-122">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="6551f-123">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="6551f-123">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="6551f-124">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="6551f-124">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="6551f-125">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="6551f-125">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="6551f-126">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="6551f-126">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="6551f-127">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="6551f-127">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="6551f-128">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="6551f-128">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="6551f-129">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="6551f-129">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="6551f-130">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="6551f-130">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="6551f-131">Требования</span><span class="sxs-lookup"><span data-stu-id="6551f-131">Requirements</span></span>



| <span data-ttu-id="6551f-132">Требование</span><span class="sxs-lookup"><span data-stu-id="6551f-132">Requirement</span></span> | <span data-ttu-id="6551f-133">Значение</span><span class="sxs-lookup"><span data-stu-id="6551f-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6551f-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6551f-134">Minimum supported client</span></span><br/> | <span data-ttu-id="6551f-135">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="6551f-135">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="6551f-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6551f-136">Minimum supported server</span></span><br/> | <span data-ttu-id="6551f-137">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="6551f-137">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6551f-138">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="6551f-138">Namespace</span></span><br/>                | <span data-ttu-id="6551f-139">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="6551f-139">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="6551f-140">MOF</span><span class="sxs-lookup"><span data-stu-id="6551f-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6551f-141"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6551f-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6551f-142">DLL</span><span class="sxs-lookup"><span data-stu-id="6551f-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6551f-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6551f-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6551f-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6551f-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6551f-145">**Мсвм \_ виртуалсистемманажементсервице**</span><span class="sxs-lookup"><span data-stu-id="6551f-145">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




