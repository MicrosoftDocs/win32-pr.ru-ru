---
title: Свойство Канресизе Ивмдисплай (Впккоминтерфацес. h)
description: Определяет, допускает ли гостевое изменение разрешение изменений.
ms.assetid: 97f2aad9-aa27-4db2-ac5d-fa9645f0e674
keywords:
- Канресизе свойство Virtual PC
- Канресизе свойство Virtual PC, интерфейс Ивмдисплай
- Ивмдисплай интерфейс Virtual PC, свойство Канресизе
topic_type:
- apiref
api_name:
- IVMDisplay.CanResize
- IVMDisplay.get_CanResize
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca865189b1fd155e0edf85bac9a36d94ffe5d656
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803754"
---
# <a name="ivmdisplaycanresize-property"></a><span data-ttu-id="fc518-106">Свойство Ивмдисплай:: Канресизе</span><span class="sxs-lookup"><span data-stu-id="fc518-106">IVMDisplay::CanResize property</span></span>

<span data-ttu-id="fc518-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="fc518-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="fc518-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="fc518-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="fc518-109">Определяет, допускает ли гостевое изменение разрешение изменений.</span><span class="sxs-lookup"><span data-stu-id="fc518-109">Determines whether the Guest allows resolution changes.</span></span>

<span data-ttu-id="fc518-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="fc518-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc518-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fc518-111">Syntax</span></span>


```C++
HRESULT get_CanResize(
  [out, retval] VARIANT_BOOL *canResize
);
```



## <a name="property-value"></a><span data-ttu-id="fc518-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="fc518-112">Property value</span></span>

<span data-ttu-id="fc518-113">**Вариант \_ Значение TRUE** , если гостевая ОС допускает изменения разрешения и **вариант \_ false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="fc518-113">**VARIANT\_TRUE** if the Guest allows resolution changes and **VARIANT\_FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="fc518-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="fc518-114">Error codes</span></span>



| <span data-ttu-id="fc518-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="fc518-115">Name/value</span></span>                                                                                                                                                                       | <span data-ttu-id="fc518-116">Значение</span><span class="sxs-lookup"><span data-stu-id="fc518-116">Meaning</span></span>                                                                                                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="fc518-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="fc518-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="fc518-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="fc518-118">The operation was successful.</span></span><br/>                                                                                                              |
| <dl> <span data-ttu-id="fc518-119"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="fc518-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="fc518-120">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="fc518-120">The parameter is **NULL**.</span></span><br/>                                                                                                                 |
| <dl> <span data-ttu-id="fc518-121"><dt>Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="fc518-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>                    | <span data-ttu-id="fc518-122">Конфигурация неизвестна.</span><span class="sxs-lookup"><span data-stu-id="fc518-122">The configuration is unknown.</span></span><br/>                                                                                                              |
| <dl> <span data-ttu-id="fc518-123"><dt>Виртуальная машина \_ \_Виртуальная машина E \_ не \_ работает</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="fc518-123"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="fc518-124">Для этой операции должна быть запущена виртуальная машина.</span><span class="sxs-lookup"><span data-stu-id="fc518-124">The virtual machine must be running for this operation.</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="fc518-125"><dt>Виртуальная машина \_ \_Нет \_ отображаемых</dt> <dt>0xA0040850</dt></span><span class="sxs-lookup"><span data-stu-id="fc518-125"><dt>VM\_E\_NO\_DISPLAY</dt> <dt>0xA0040850</dt></span></span> </dl>                    | <span data-ttu-id="fc518-126">Не найдено видеоадаптеров для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="fc518-126">There was no video device found for the virtual machine.</span></span><br/>                                                                                   |
| <dl> <span data-ttu-id="fc518-127"><dt>Виртуальная машина \_ Добавление компонента "E" \_ \_ \_ не \_ </dt> доступно <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="fc518-127"><dt>VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="fc518-128">Компонент интеграции недоступен; либо компоненты интеграции не установлены, либо функция отключена.</span><span class="sxs-lookup"><span data-stu-id="fc518-128">The integration components feature is not available; either the integration components are not installed or the feature has been disabled.</span></span><br/> |
| <dl> <span data-ttu-id="fc518-129"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="fc518-129"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="fc518-130">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="fc518-130">An unexpected error has occurred.</span></span><br/>                                                                                                          |



## <a name="requirements"></a><span data-ttu-id="fc518-131">Требования</span><span class="sxs-lookup"><span data-stu-id="fc518-131">Requirements</span></span>



| <span data-ttu-id="fc518-132">Требование</span><span class="sxs-lookup"><span data-stu-id="fc518-132">Requirement</span></span> | <span data-ttu-id="fc518-133">Значение</span><span class="sxs-lookup"><span data-stu-id="fc518-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc518-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fc518-134">Minimum supported client</span></span><br/> | <span data-ttu-id="fc518-135">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="fc518-135">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fc518-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fc518-136">Minimum supported server</span></span><br/> | <span data-ttu-id="fc518-137">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="fc518-137">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="fc518-138">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="fc518-138">End of client support</span></span><br/>    | <span data-ttu-id="fc518-139">Windows 7</span><span class="sxs-lookup"><span data-stu-id="fc518-139">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="fc518-140">Продукт</span><span class="sxs-lookup"><span data-stu-id="fc518-140">Product</span></span><br/>                  | <span data-ttu-id="fc518-141">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="fc518-141">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="fc518-142">Header</span><span class="sxs-lookup"><span data-stu-id="fc518-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="fc518-143"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc518-143"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="fc518-144">IID</span><span class="sxs-lookup"><span data-stu-id="fc518-144">IID</span></span><br/>                      | <span data-ttu-id="fc518-145">IID \_ ивмдисплай определен как 960895e9-f743-4498-96aa-261f867e7fc5</span><span class="sxs-lookup"><span data-stu-id="fc518-145">IID\_IVMDisplay is defined as 960895e9-f743-4498-96aa-261f867e7fc5</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="fc518-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fc518-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc518-147">**ивмдисплай**</span><span class="sxs-lookup"><span data-stu-id="fc518-147">**IVMDisplay**</span></span>](ivmdisplay.md)
</dt> </dl>

 

