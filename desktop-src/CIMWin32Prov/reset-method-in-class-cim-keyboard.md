---
description: Метод Reset \_ класса клавиатуры CIM запрашивает сброс логического устройства.
ms.assetid: 737bd50c-8e40-4f60-9deb-587b6f37c151
ms.tgt_platform: multiple
title: Метод Reset класса CIM_Keyboard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Keyboard.Reset
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8e5296953e157182c97e113539b1b47625a0de44
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990658"
---
# <a name="reset-method-of-the-cim_keyboard-class"></a><span data-ttu-id="87d91-103">Метод Reset \_ класса клавиатуры CIM</span><span class="sxs-lookup"><span data-stu-id="87d91-103">Reset method of the CIM\_Keyboard class</span></span>

<span data-ttu-id="87d91-104">Метод **Reset** \_ класса клавиатуры CIM запрашивает сброс логического устройства.</span><span class="sxs-lookup"><span data-stu-id="87d91-104">The **Reset** method of the CIM\_Keyboard class requests a reset of the logical device.</span></span> <span data-ttu-id="87d91-105">Этот метод наследуется [**от \_ CIM**](cim-logicaldevice.md)-ого модели.</span><span class="sxs-lookup"><span data-stu-id="87d91-105">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="87d91-106">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="87d91-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="87d91-107">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="87d91-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="87d91-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="87d91-108">Syntax</span></span>


```mof
uint32 Reset();
```



## <a name="parameters"></a><span data-ttu-id="87d91-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="87d91-109">Parameters</span></span>

<span data-ttu-id="87d91-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="87d91-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="87d91-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="87d91-111">Return value</span></span>

<span data-ttu-id="87d91-112">Возвращает 0 (ноль), если запрос был успешно выполнен, 1 (один), если запрос не поддерживается, и другое значение, если произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="87d91-112">Returns 0 (zero) if the request was successfully executed, 1 (one) if the request is not supported, and some other value if an error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="87d91-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="87d91-113">Remarks</span></span>

<span data-ttu-id="87d91-114">В настоящее время этот метод не реализован инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="87d91-114">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="87d91-115">Чтобы использовать этот метод, его необходимо реализовать в собственном поставщике.</span><span class="sxs-lookup"><span data-stu-id="87d91-115">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="87d91-116">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="87d91-116">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="87d91-117">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="87d91-117">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="87d91-118">Требования</span><span class="sxs-lookup"><span data-stu-id="87d91-118">Requirements</span></span>



| <span data-ttu-id="87d91-119">Требование</span><span class="sxs-lookup"><span data-stu-id="87d91-119">Requirement</span></span> | <span data-ttu-id="87d91-120">Значение</span><span class="sxs-lookup"><span data-stu-id="87d91-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="87d91-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="87d91-121">Minimum supported client</span></span><br/> | <span data-ttu-id="87d91-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="87d91-122">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="87d91-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="87d91-123">Minimum supported server</span></span><br/> | <span data-ttu-id="87d91-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="87d91-124">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="87d91-125">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="87d91-125">Namespace</span></span><br/>                | <span data-ttu-id="87d91-126">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="87d91-126">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="87d91-127">MOF</span><span class="sxs-lookup"><span data-stu-id="87d91-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="87d91-128"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="87d91-128"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="87d91-129">DLL</span><span class="sxs-lookup"><span data-stu-id="87d91-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="87d91-130"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="87d91-130"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87d91-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="87d91-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87d91-132">\_Клавиатура CIM</span><span class="sxs-lookup"><span data-stu-id="87d91-132">CIM\_Keyboard</span></span>](reset-method-in-class-cim-keyboard.md)
</dt> <dt>

[<span data-ttu-id="87d91-133">**\_Клавиатура CIM**</span><span class="sxs-lookup"><span data-stu-id="87d91-133">**CIM\_Keyboard**</span></span>](cim-keyboard.md)
</dt> </dl>

 

 




