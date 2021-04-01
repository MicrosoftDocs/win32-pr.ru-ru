---
title: Свойство Унконнектеднетворкадаптерс Ивмвиртуалпк (Впккоминтерфацес. h)
description: Возвращает перечисляемую коллекцию неподключенных сетевых интерфейсов.
ms.assetid: 2d95f289-083a-4388-b842-0a11b4e1a06f
keywords:
- Унконнектеднетворкадаптерс свойство Virtual PC
- Унконнектеднетворкадаптерс свойство Virtual PC, интерфейс Ивмвиртуалпк
- Ивмвиртуалпк интерфейс Virtual PC, свойство Унконнектеднетворкадаптерс
topic_type:
- apiref
api_name:
- IVMVirtualPC.UnconnectedNetworkAdapters
- IVMVirtualPC.get_UnconnectedNetworkAdapters
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0694c6c5ce782e05ca322ba57f4ce7aaf5f708d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071750"
---
# <a name="ivmvirtualpcunconnectednetworkadapters-property"></a><span data-ttu-id="d780c-106">Свойство Ивмвиртуалпк:: Унконнектеднетворкадаптерс</span><span class="sxs-lookup"><span data-stu-id="d780c-106">IVMVirtualPC::UnconnectedNetworkAdapters property</span></span>

<span data-ttu-id="d780c-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="d780c-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="d780c-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="d780c-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="d780c-109">Возвращает перечисляемую коллекцию неподключенных сетевых интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="d780c-109">Retrieves an enumerable collection of unconnected network interfaces.</span></span>

<span data-ttu-id="d780c-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="d780c-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d780c-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d780c-111">Syntax</span></span>


```C++
HRESULT get_UnconnectedNetworkAdapters(
  [out, retval] IVMNetworkAdapterCollection **unconnectedNetworkAdapterCollection
);
```



## <a name="property-value"></a><span data-ttu-id="d780c-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="d780c-112">Property value</span></span>

<span data-ttu-id="d780c-113">Коллекция неподключенных объектов [**ивмнетворкадаптер**](ivmnetworkadapter.md) .</span><span class="sxs-lookup"><span data-stu-id="d780c-113">A collection of unconnected [**IVMNetworkAdapter**](ivmnetworkadapter.md) objects.</span></span> <span data-ttu-id="d780c-114">См. [**ивмнетворкадаптерколлектион**](ivmnetworkadaptercollection.md).</span><span class="sxs-lookup"><span data-stu-id="d780c-114">See [**IVMNetworkAdapterCollection**](ivmnetworkadaptercollection.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="d780c-115">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="d780c-115">Error codes</span></span>



| <span data-ttu-id="d780c-116">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="d780c-116">Name/value</span></span>                                                                                                                                                                           | <span data-ttu-id="d780c-117">Значение</span><span class="sxs-lookup"><span data-stu-id="d780c-117">Meaning</span></span>                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d780c-118"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="d780c-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="d780c-119">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="d780c-119">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="d780c-120"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="d780c-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="d780c-121">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="d780c-121">The parameter is **NULL**.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="d780c-122"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="d780c-122"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="d780c-123">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="d780c-123">An unexpected error has occurred.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="d780c-124"><dt>Виртуальная машина \_ E \_ аппаратная \_ виртуализация \_ отключена</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="d780c-124"><dt>VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="d780c-125">Процессор не поддерживает расширения виртуализации с аппаратным ускорением (ЗАКОНЧИТЕ).</span><span class="sxs-lookup"><span data-stu-id="d780c-125">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="d780c-126">Требования</span><span class="sxs-lookup"><span data-stu-id="d780c-126">Requirements</span></span>



| <span data-ttu-id="d780c-127">Требование</span><span class="sxs-lookup"><span data-stu-id="d780c-127">Requirement</span></span> | <span data-ttu-id="d780c-128">Значение</span><span class="sxs-lookup"><span data-stu-id="d780c-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d780c-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d780c-129">Minimum supported client</span></span><br/> | <span data-ttu-id="d780c-130">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="d780c-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d780c-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d780c-131">Minimum supported server</span></span><br/> | <span data-ttu-id="d780c-132">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="d780c-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="d780c-133">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="d780c-133">End of client support</span></span><br/>    | <span data-ttu-id="d780c-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d780c-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="d780c-135">Продукт</span><span class="sxs-lookup"><span data-stu-id="d780c-135">Product</span></span><br/>                  | <span data-ttu-id="d780c-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="d780c-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="d780c-137">Header</span><span class="sxs-lookup"><span data-stu-id="d780c-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="d780c-138"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="d780c-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="d780c-139">IID</span><span class="sxs-lookup"><span data-stu-id="d780c-139">IID</span></span><br/>                      | <span data-ttu-id="d780c-140">IID \_ ивмвиртуалпк определен как 236ba0d9-a24a-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="d780c-140">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="d780c-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d780c-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d780c-142">**ивмвиртуалпк**</span><span class="sxs-lookup"><span data-stu-id="d780c-142">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

