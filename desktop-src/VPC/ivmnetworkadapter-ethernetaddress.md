---
title: Свойство Есернетаддресс Ивмнетворкадаптер (Впккоминтерфацес. h)
description: Ethernet-адрес сетевого интерфейса.
ms.assetid: 2d94c5b3-6b69-4fb1-bee4-081dc026dde3
keywords:
- Есернетаддресс свойство Virtual PC
- Есернетаддресс свойство Virtual PC, интерфейс Ивмнетворкадаптер
- Ивмнетворкадаптер интерфейс Virtual PC, свойство Есернетаддресс
topic_type:
- apiref
api_name:
- IVMNetworkAdapter.EthernetAddress
- IVMNetworkAdapter.get_EthernetAddress
- IVMNetworkAdapter.put_EthernetAddress
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7afb8f9035b0a663e01eeead95dc3f4f6bdec2e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103800970"
---
# <a name="ivmnetworkadapterethernetaddress-property"></a><span data-ttu-id="119c8-106">Свойство Ивмнетворкадаптер:: Есернетаддресс</span><span class="sxs-lookup"><span data-stu-id="119c8-106">IVMNetworkAdapter::EthernetAddress property</span></span>

<span data-ttu-id="119c8-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="119c8-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="119c8-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="119c8-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="119c8-109">Извлекает и устанавливает адрес Ethernet (MAC) сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="119c8-109">Retrieves and sets the Ethernet (MAC) address of the network interface.</span></span>

<span data-ttu-id="119c8-110">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="119c8-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="119c8-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="119c8-111">Syntax</span></span>


```C++
HRESULT put_EthernetAddress(
  [in]          BSTR ethernetAddress
);

HRESULT get_EthernetAddress(
  [out, retval] BSTR *ethernetAddress
);
```



## <a name="property-value"></a><span data-ttu-id="119c8-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="119c8-112">Property value</span></span>

<span data-ttu-id="119c8-113">MAC-адрес виртуального сетевого адаптера.</span><span class="sxs-lookup"><span data-stu-id="119c8-113">The MAC address of the virtual NIC.</span></span> <span data-ttu-id="119c8-114">Он должен иметь форму "*XX* - *XX* - *XX* - *XX*, XX -  - ", где каждый *X* является шестнадцатеричной цифрой.</span><span class="sxs-lookup"><span data-stu-id="119c8-114">It should have the form "*XX*-*XX*-*XX*-*XX*-*XX*-*XX*" where each *X* is a hexadecimal digit.</span></span>

## <a name="error-codes"></a><span data-ttu-id="119c8-115">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="119c8-115">Error codes</span></span>



| <span data-ttu-id="119c8-116">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="119c8-116">Name/value</span></span>                                                                                                                                                                         | <span data-ttu-id="119c8-117">Значение</span><span class="sxs-lookup"><span data-stu-id="119c8-117">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="119c8-118"><dt>\_ОК</dt></span><span class="sxs-lookup"><span data-stu-id="119c8-118"><dt>S\_OK</dt></span></span> </dl>                                                                                                   | <span data-ttu-id="119c8-119">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="119c8-119">The operation was successful.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                    |
| <dl> <span data-ttu-id="119c8-120"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="119c8-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                              | <span data-ttu-id="119c8-121">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="119c8-121">The parameter is **NULL**.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="119c8-122"><dt>Д \_ INVALIDARG</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="119c8-122"><dt>E\_INVALIDARG</dt> <dt>0x80000003</dt></span></span> </dl>                           | <span data-ttu-id="119c8-123">Неправильный формат параметра.</span><span class="sxs-lookup"><span data-stu-id="119c8-123">The parameter is not in the correct format.</span></span><br/>                                                                                                                                                                                                                                                                                                                                      |
| <dl> <span data-ttu-id="119c8-124"><dt>Виртуальная машина \_ E не \_ удается \_ задать \_ динамический \_ Mac- \_ адрес</dt> <dt>0xA004070A</dt></span><span class="sxs-lookup"><span data-stu-id="119c8-124"><dt>VM\_E\_CANT\_SET\_DYNAMIC\_MAC\_ADDRESS</dt> <dt>0xA004070A</dt></span></span> </dl> | <span data-ttu-id="119c8-125">Адрес Ethernet для сетевого интерфейса может быть создан динамически или может быть задан статическим адресом пользователя.</span><span class="sxs-lookup"><span data-stu-id="119c8-125">The Ethernet address for a network interface can either be generated dynamically or can be set to a static address by the user.</span></span> <span data-ttu-id="119c8-126">Этот метод не может быть вызван, если адрес настроен для динамического создания.</span><span class="sxs-lookup"><span data-stu-id="119c8-126">This method cannot be called when the address is set to be generated dynamically.</span></span> <span data-ttu-id="119c8-127">Свойство [**исесернетаддрессдинамик**](ivmnetworkadapter-isethernetaddressdynamic.md) используется для изменения поведения при создании адреса Ethernet.</span><span class="sxs-lookup"><span data-stu-id="119c8-127">The [**IsEthernetAddressDynamic**](ivmnetworkadapter-isethernetaddressdynamic.md) property is used to change the generation behavior of the Ethernet address.</span></span><br/> |
| <dl> <span data-ttu-id="119c8-128"><dt>Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="119c8-128"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>                      | <span data-ttu-id="119c8-129">Виртуальная машина не найдена.</span><span class="sxs-lookup"><span data-stu-id="119c8-129">The virtual machine was not found.</span></span> <span data-ttu-id="119c8-130">Это может произойти, если компьютер был удален после создания объекта [**ивмнетворкадаптер**](ivmnetworkadapter.md) .</span><span class="sxs-lookup"><span data-stu-id="119c8-130">This may occur if the machine was removed after the [**IVMNetworkAdapter**](ivmnetworkadapter.md) object was created.</span></span><br/>                                                                                                                                                                                                                        |
| <dl> <span data-ttu-id="119c8-131"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="119c8-131"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                      | <span data-ttu-id="119c8-132">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="119c8-132">An unexpected error has occurred.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                |



## <a name="requirements"></a><span data-ttu-id="119c8-133">Требования</span><span class="sxs-lookup"><span data-stu-id="119c8-133">Requirements</span></span>



| <span data-ttu-id="119c8-134">Требование</span><span class="sxs-lookup"><span data-stu-id="119c8-134">Requirement</span></span> | <span data-ttu-id="119c8-135">Значение</span><span class="sxs-lookup"><span data-stu-id="119c8-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="119c8-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="119c8-136">Minimum supported client</span></span><br/> | <span data-ttu-id="119c8-137">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="119c8-137">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="119c8-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="119c8-138">Minimum supported server</span></span><br/> | <span data-ttu-id="119c8-139">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="119c8-139">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="119c8-140">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="119c8-140">End of client support</span></span><br/>    | <span data-ttu-id="119c8-141">Windows 7</span><span class="sxs-lookup"><span data-stu-id="119c8-141">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="119c8-142">Продукт</span><span class="sxs-lookup"><span data-stu-id="119c8-142">Product</span></span><br/>                  | <span data-ttu-id="119c8-143">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="119c8-143">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="119c8-144">Header</span><span class="sxs-lookup"><span data-stu-id="119c8-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="119c8-145"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="119c8-145"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="119c8-146">IID</span><span class="sxs-lookup"><span data-stu-id="119c8-146">IID</span></span><br/>                      | <span data-ttu-id="119c8-147">IID \_ ивмнетворкадаптер определен как e32e4165-22b8-4DC0-8d57-850171ae207a</span><span class="sxs-lookup"><span data-stu-id="119c8-147">IID\_IVMNetworkAdapter is defined as e32e4165-22b8-4dc0-8d57-850171ae207a</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="119c8-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="119c8-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="119c8-149">**ивмнетворкадаптер**</span><span class="sxs-lookup"><span data-stu-id="119c8-149">**IVMNetworkAdapter**</span></span>](ivmnetworkadapter.md)
</dt> </dl>

 

