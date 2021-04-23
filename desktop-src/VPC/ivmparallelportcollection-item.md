---
title: Свойство Item Ивмпараллелпортколлектион (Впккоминтерфацес. h)
description: Извлекает объект параллельного порта, соответствующий указанному индексу.
ms.assetid: f67a4224-ca96-4d68-9f0f-4977ffff859e
keywords:
- Свойство элемента Virtual PC
- Свойство элемента Virtual PC, интерфейс Ивмпараллелпортколлектион
- Интерфейс Ивмпараллелпортколлектион Virtual PC, свойство Item
topic_type:
- apiref
api_name:
- IVMParallelPortCollection.Item
- IVMParallelPortCollection.get_Item
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: daa450f1859db8af6ed884b37fc693fc4fb1990f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492585"
---
# <a name="ivmparallelportcollectionitem-property"></a><span data-ttu-id="b11e5-106">Свойство Ивмпараллелпортколлектион:: Item</span><span class="sxs-lookup"><span data-stu-id="b11e5-106">IVMParallelPortCollection::Item property</span></span>

<span data-ttu-id="b11e5-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="b11e5-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="b11e5-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="b11e5-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="b11e5-109">Извлекает объект параллельного порта, соответствующий указанному индексу.</span><span class="sxs-lookup"><span data-stu-id="b11e5-109">Retrieves the parallel port object that corresponds to the specified index.</span></span>

<span data-ttu-id="b11e5-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="b11e5-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b11e5-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b11e5-111">Syntax</span></span>


```C++
HRESULT get_Item(
  [in]          long            index,
  [out, retval] IVMParallelPort **vmParallelPort
);
```



## <a name="property-value"></a><span data-ttu-id="b11e5-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="b11e5-112">Property value</span></span>

<span data-ttu-id="b11e5-113">Объект [**ивмпараллелпорт**](ivmparallelport.md) .</span><span class="sxs-lookup"><span data-stu-id="b11e5-113">The [**IVMParallelPort**](ivmparallelport.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b11e5-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="b11e5-114">Error codes</span></span>



| <span data-ttu-id="b11e5-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="b11e5-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="b11e5-116">Значение</span><span class="sxs-lookup"><span data-stu-id="b11e5-116">Meaning</span></span>                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b11e5-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b11e5-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="b11e5-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="b11e5-118">The operation was successful.</span></span> <br/>                                                      |
| <dl> <span data-ttu-id="b11e5-119"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="b11e5-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="b11e5-120">Параметр *вмпараллелпорт* имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="b11e5-120">The *vmParallelPort* parameter is **NULL**.</span></span> <br/>                                        |
| <dl> <span data-ttu-id="b11e5-121"><dt> \_ E \_ бадиндекс</dt> <dt>0x8002000B</dt></span><span class="sxs-lookup"><span data-stu-id="b11e5-121"><dt>DISP\_E\_BADINDEX</dt> <dt>0x8002000B</dt></span></span> </dl>  | <span data-ttu-id="b11e5-122">Индекс запрошенного элемента не соответствует элементу в этой коллекции.</span><span class="sxs-lookup"><span data-stu-id="b11e5-122">The index of the requested item does not correspond to an item in this collection.</span></span> <br/> |
| <dl> <span data-ttu-id="b11e5-123"><dt>Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="b11e5-123"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="b11e5-124">Конфигурация неизвестна.</span><span class="sxs-lookup"><span data-stu-id="b11e5-124">The configuration is unknown.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="b11e5-125"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="b11e5-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="b11e5-126">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="b11e5-126">An unexpected error has occurred.</span></span><br/>                                                   |



## <a name="requirements"></a><span data-ttu-id="b11e5-127">Требования</span><span class="sxs-lookup"><span data-stu-id="b11e5-127">Requirements</span></span>



| <span data-ttu-id="b11e5-128">Требование</span><span class="sxs-lookup"><span data-stu-id="b11e5-128">Requirement</span></span> | <span data-ttu-id="b11e5-129">Значение</span><span class="sxs-lookup"><span data-stu-id="b11e5-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b11e5-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b11e5-130">Minimum supported client</span></span><br/> | <span data-ttu-id="b11e5-131">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="b11e5-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b11e5-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b11e5-132">Minimum supported server</span></span><br/> | <span data-ttu-id="b11e5-133">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="b11e5-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="b11e5-134">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="b11e5-134">End of client support</span></span><br/>    | <span data-ttu-id="b11e5-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b11e5-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="b11e5-136">Продукт</span><span class="sxs-lookup"><span data-stu-id="b11e5-136">Product</span></span><br/>                  | <span data-ttu-id="b11e5-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="b11e5-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="b11e5-138">Header</span><span class="sxs-lookup"><span data-stu-id="b11e5-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="b11e5-139"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="b11e5-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="b11e5-140">IID</span><span class="sxs-lookup"><span data-stu-id="b11e5-140">IID</span></span><br/>                      | <span data-ttu-id="b11e5-141">IID \_ ивмпараллелпортколлектион определен как 27c3e036-198f-430c-8735-6e652f7203fd</span><span class="sxs-lookup"><span data-stu-id="b11e5-141">IID\_IVMParallelPortCollection is defined as 27c3e036-198f-430c-8735-6e652f7203fd</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="b11e5-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b11e5-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b11e5-143">**ивмпараллелпорт**</span><span class="sxs-lookup"><span data-stu-id="b11e5-143">**IVMParallelPort**</span></span>](ivmparallelport.md)
</dt> <dt>

[<span data-ttu-id="b11e5-144">**ивмпараллелпортколлектион**</span><span class="sxs-lookup"><span data-stu-id="b11e5-144">**IVMParallelPortCollection**</span></span>](ivmparallelportcollection.md)
</dt> </dl>

 

