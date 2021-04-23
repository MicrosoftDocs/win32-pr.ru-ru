---
title: Свойство Item Ивмхарддискконнектионколлектион (Впккоминтерфацес. h)
description: Извлекает объект подключения к жесткому диску, соответствующий указанному индексу.
ms.assetid: 24e158fb-b026-4619-9d0d-a59cd782894f
keywords:
- Свойство элемента Virtual PC
- Свойство элемента Virtual PC, интерфейс Ивмхарддискконнектионколлектион
- Интерфейс Ивмхарддискконнектионколлектион Virtual PC, свойство Item
topic_type:
- apiref
api_name:
- IVMHardDiskConnectionCollection.Item
- IVMHardDiskConnectionCollection.get_Item
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5558e70cfcf18f67c14e52160737b851fa9ea2c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672457"
---
# <a name="ivmharddiskconnectioncollectionitem-property"></a><span data-ttu-id="7c322-106">Свойство Ивмхарддискконнектионколлектион:: Item</span><span class="sxs-lookup"><span data-stu-id="7c322-106">IVMHardDiskConnectionCollection::Item property</span></span>

<span data-ttu-id="7c322-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="7c322-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="7c322-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="7c322-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="7c322-109">Извлекает объект подключения к жесткому диску, соответствующий указанному индексу.</span><span class="sxs-lookup"><span data-stu-id="7c322-109">Retrieves the hard disk connection object that corresponds to the specified index.</span></span>

<span data-ttu-id="7c322-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="7c322-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c322-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7c322-111">Syntax</span></span>


```C++
HRESULT get_Item(
  [in]          long                  index,
  [out, retval] IVMHardDiskConnection **hardDiskConnection
);
```



## <a name="property-value"></a><span data-ttu-id="7c322-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="7c322-112">Property value</span></span>

<span data-ttu-id="7c322-113">Объект [**ивмхарддискконнектион**](ivmharddiskconnection.md) .</span><span class="sxs-lookup"><span data-stu-id="7c322-113">The [**IVMHardDiskConnection**](ivmharddiskconnection.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="7c322-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="7c322-114">Error codes</span></span>



| <span data-ttu-id="7c322-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="7c322-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="7c322-116">Значение</span><span class="sxs-lookup"><span data-stu-id="7c322-116">Meaning</span></span>                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7c322-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="7c322-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="7c322-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="7c322-118">The operation was successful.</span></span> <br/>                                                      |
| <dl> <span data-ttu-id="7c322-119"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="7c322-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="7c322-120">Параметр *харддискконнектион* имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="7c322-120">The *hardDiskConnection* parameter is **NULL**.</span></span> <br/>                                    |
| <dl> <span data-ttu-id="7c322-121"><dt> \_ E \_ бадиндекс</dt> <dt>0x8002000B</dt></span><span class="sxs-lookup"><span data-stu-id="7c322-121"><dt>DISP\_E\_BADINDEX</dt> <dt>0x8002000B</dt></span></span> </dl>  | <span data-ttu-id="7c322-122">Индекс запрошенного элемента не соответствует элементу в этой коллекции.</span><span class="sxs-lookup"><span data-stu-id="7c322-122">The index of the requested item does not correspond to an item in this collection.</span></span> <br/> |
| <dl> <span data-ttu-id="7c322-123"><dt>Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="7c322-123"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="7c322-124">Конфигурация неизвестна.</span><span class="sxs-lookup"><span data-stu-id="7c322-124">The configuration is unknown.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="7c322-125"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="7c322-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="7c322-126">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="7c322-126">An unexpected error has occurred.</span></span><br/>                                                   |



## <a name="requirements"></a><span data-ttu-id="7c322-127">Требования</span><span class="sxs-lookup"><span data-stu-id="7c322-127">Requirements</span></span>



| <span data-ttu-id="7c322-128">Требование</span><span class="sxs-lookup"><span data-stu-id="7c322-128">Requirement</span></span> | <span data-ttu-id="7c322-129">Значение</span><span class="sxs-lookup"><span data-stu-id="7c322-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c322-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7c322-130">Minimum supported client</span></span><br/> | <span data-ttu-id="7c322-131">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="7c322-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                         |
| <span data-ttu-id="7c322-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7c322-132">Minimum supported server</span></span><br/> | <span data-ttu-id="7c322-133">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="7c322-133">None supported</span></span><br/>                                                                          |
| <span data-ttu-id="7c322-134">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="7c322-134">End of client support</span></span><br/>    | <span data-ttu-id="7c322-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="7c322-135">Windows 7</span></span><br/>                                                                               |
| <span data-ttu-id="7c322-136">Продукт</span><span class="sxs-lookup"><span data-stu-id="7c322-136">Product</span></span><br/>                  | <span data-ttu-id="7c322-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="7c322-137">Windows Virtual PC</span></span><br/>                                                                      |
| <span data-ttu-id="7c322-138">Header</span><span class="sxs-lookup"><span data-stu-id="7c322-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c322-139"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c322-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl>      |
| <span data-ttu-id="7c322-140">IID</span><span class="sxs-lookup"><span data-stu-id="7c322-140">IID</span></span><br/>                      | <span data-ttu-id="7c322-141">IID \_ ивмхарддискконнектионколлектион определен как b9f2caf4-0aeb-4085-B105-ceddb90dbf62</span><span class="sxs-lookup"><span data-stu-id="7c322-141">IID\_IVMHardDiskconnectionCollection is defined as b9f2caf4-0aeb-4085-b105-ceddb90dbf62</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7c322-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7c322-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c322-143">**ивмхарддискконнектион**</span><span class="sxs-lookup"><span data-stu-id="7c322-143">**IVMHardDiskConnection**</span></span>](ivmharddiskconnection.md)
</dt> <dt>

[<span data-ttu-id="7c322-144">**ивмхарддискконнектионколлектион**</span><span class="sxs-lookup"><span data-stu-id="7c322-144">**IVMHardDiskConnectionCollection**</span></span>](ivmharddiskconnectioncollection.md)
</dt> </dl>

 

