---
title: Интерфейс Ивмвиртуалпцевентс (Впккоминтерфацес. h)
description: Определяет интерфейс исходящего события для интерфейса Ивмвиртуалпк.
ms.assetid: 40ce14d8-43e4-4c72-9729-e5503d882be6
keywords:
- Виртуальный ПК с интерфейсом Ивмвиртуалпцевентс
- Ивмвиртуалпцевентс интерфейс Virtual PC, описание
topic_type:
- apiref
api_name:
- IVMVirtualPCEvents
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c3a6fd22f75027d1424b8605e8e36e373064069
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071865"
---
# <a name="ivmvirtualpcevents-interface"></a><span data-ttu-id="cbc84-105">Интерфейс Ивмвиртуалпцевентс</span><span class="sxs-lookup"><span data-stu-id="cbc84-105">IVMVirtualPCEvents interface</span></span>

<span data-ttu-id="cbc84-106">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="cbc84-106">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="cbc84-107">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="cbc84-107">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="cbc84-108">Определяет интерфейс исходящего события для интерфейса [**ивмвиртуалпк**](ivmvirtualpc.md) .</span><span class="sxs-lookup"><span data-stu-id="cbc84-108">Defines the outgoing event interface for the [**IVMVirtualPC**](ivmvirtualpc.md) interface.</span></span> <span data-ttu-id="cbc84-109">Клиент реализует эти методы для получения событий, отправленных из [**ивмвиртуалпк**](ivmvirtualpc.md).</span><span class="sxs-lookup"><span data-stu-id="cbc84-109">The client implements these methods to receive events sent from [**IVMVirtualPC**](ivmvirtualpc.md).</span></span>

## <a name="members"></a><span data-ttu-id="cbc84-110">Элементы</span><span class="sxs-lookup"><span data-stu-id="cbc84-110">Members</span></span>

<span data-ttu-id="cbc84-111">Интерфейс **ивмвиртуалпцевентс** наследует от интерфейса [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="cbc84-111">The **IVMVirtualPCEvents** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="cbc84-112">**Ивмвиртуалпцевентс** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="cbc84-112">**IVMVirtualPCEvents** also has these types of members:</span></span>

-   [<span data-ttu-id="cbc84-113">Методы</span><span class="sxs-lookup"><span data-stu-id="cbc84-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="cbc84-114">Методы</span><span class="sxs-lookup"><span data-stu-id="cbc84-114">Methods</span></span>

<span data-ttu-id="cbc84-115">Интерфейс **ивмвиртуалпцевентс** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="cbc84-115">The **IVMVirtualPCEvents** interface has these methods.</span></span>



| <span data-ttu-id="cbc84-116">Метод</span><span class="sxs-lookup"><span data-stu-id="cbc84-116">Method</span></span>                                                        | <span data-ttu-id="cbc84-117">Описание</span><span class="sxs-lookup"><span data-stu-id="cbc84-117">Description</span></span>                                                                  |
|:--------------------------------------------------------------|:-----------------------------------------------------------------------------|
| [<span data-ttu-id="cbc84-118">**оневентлогжед**</span><span class="sxs-lookup"><span data-stu-id="cbc84-118">**OnEventLogged**</span></span>](ivmvirtualpcevents-oneventlogged.md)     | <span data-ttu-id="cbc84-119">Получает уведомление о том, что Windows Virtual PC регистрирует событие.</span><span class="sxs-lookup"><span data-stu-id="cbc84-119">Receives notification that Windows Virtual PC logs an event.</span></span><br/>      |
| [<span data-ttu-id="cbc84-120">**онвмстатечанже**</span><span class="sxs-lookup"><span data-stu-id="cbc84-120">**OnVMStateChange**</span></span>](ivmvirtualpcevents-onvmstatechange.md) | <span data-ttu-id="cbc84-121">Получает уведомление о том, что состояние виртуальной машины изменилось.</span><span class="sxs-lookup"><span data-stu-id="cbc84-121">Receives notification that a virtual machine's state has changed.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="cbc84-122">Требования</span><span class="sxs-lookup"><span data-stu-id="cbc84-122">Requirements</span></span>



| <span data-ttu-id="cbc84-123">Требование</span><span class="sxs-lookup"><span data-stu-id="cbc84-123">Requirement</span></span> | <span data-ttu-id="cbc84-124">Значение</span><span class="sxs-lookup"><span data-stu-id="cbc84-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbc84-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cbc84-125">Minimum supported client</span></span><br/> | <span data-ttu-id="cbc84-126">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="cbc84-126">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="cbc84-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cbc84-127">Minimum supported server</span></span><br/> | <span data-ttu-id="cbc84-128">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="cbc84-128">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="cbc84-129">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="cbc84-129">End of client support</span></span><br/>    | <span data-ttu-id="cbc84-130">Windows 7</span><span class="sxs-lookup"><span data-stu-id="cbc84-130">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="cbc84-131">Продукт</span><span class="sxs-lookup"><span data-stu-id="cbc84-131">Product</span></span><br/>                  | <span data-ttu-id="cbc84-132">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="cbc84-132">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="cbc84-133">Header</span><span class="sxs-lookup"><span data-stu-id="cbc84-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="cbc84-134"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="cbc84-134"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="cbc84-135">IID</span><span class="sxs-lookup"><span data-stu-id="cbc84-135">IID</span></span><br/>                      | <span data-ttu-id="cbc84-136">ДИИД \_ ивмвиртуалпцевентс определяется как efed1ef1-3c09-41f7-a9c2-7e29fa286c9d</span><span class="sxs-lookup"><span data-stu-id="cbc84-136">DIID\_IVMVirtualPCEvents is defined as efed1ef1-3c09-41f7-a9c2-7e29fa286c9d</span></span><br/>        |



 

