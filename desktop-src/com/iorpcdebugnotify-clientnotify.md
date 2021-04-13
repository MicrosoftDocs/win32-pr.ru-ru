---
title: Иорпкдебугнотифи Клиентнотифи, метод
description: Информирует клиента о том, что исходящий запрос отладчика к серверу.
ms.assetid: a41e3eaa-6d1f-46bf-9103-f83e45b2cd90
keywords:
- COM-метод Клиентнотифи
- Метод Клиентнотифи COM, интерфейс Иорпкдебугнотифи
- Интерфейс Иорпкдебугнотифи COM, метод Клиентнотифи
topic_type:
- apiref
api_name:
- IOrpcDebugNotify.ClientNotify
api_location:
- N/A
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9e788a51e278df09715aaf9d4993ac5724ed65b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493083"
---
# <a name="iorpcdebugnotifyclientnotify-method"></a><span data-ttu-id="81725-106">Метод Иорпкдебугнотифи:: Клиентнотифи</span><span class="sxs-lookup"><span data-stu-id="81725-106">IOrpcDebugNotify::ClientNotify method</span></span>

<span data-ttu-id="81725-107">Информирует клиента о том, что исходящий запрос отладчика к серверу.</span><span class="sxs-lookup"><span data-stu-id="81725-107">Informs the client of an outgoing debugger request to the server.</span></span>

> [!Note]  
> <span data-ttu-id="81725-108">Библиотека импорта, содержащая функцию **клиентнотифи** , не включена в пакет средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="81725-108">An import library containing the **ClientNotify** function is not included in the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="81725-109">Приложение может использовать функции [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) и [**Ошибка GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) для получения указателя на функцию [**дллдебугобжектрпчук**](dlldebugobjectrpchook.md) из oleaut.dll и предоставления этой функции через интерфейс [**иорпкдебугнотифи**](iorpcdebugnotify.md) .</span><span class="sxs-lookup"><span data-stu-id="81725-109">An application can use the [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) and [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) functions to retrieve a function pointer to [**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md) from oleaut.dll and provide this function via the [**IOrpcDebugNotify**](iorpcdebugnotify.md) interface.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="81725-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="81725-110">Syntax</span></span>


```C++
void ClientNotify(
   ORPC_DBG_ALL *lpOrpcDebugAll
);
```



## <a name="parameters"></a><span data-ttu-id="81725-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="81725-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81725-112">*лпорпкдебугалл*</span><span class="sxs-lookup"><span data-stu-id="81725-112">*lpOrpcDebugAll*</span></span> 
</dt> <dd>

<span data-ttu-id="81725-113">Указатель на структуру [**ОРПК \_ dbg \_ ALL**](orpc-dbg-all.md) , содержащую сведения об уведомлении, которые система com RPC передает отладчику.</span><span class="sxs-lookup"><span data-stu-id="81725-113">A pointer to a [**ORPC\_DBG\_ALL**](orpc-dbg-all.md) structure that contains notification specific information the COM RPC system passes to the debugger.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81725-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="81725-114">Return value</span></span>

<span data-ttu-id="81725-115">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="81725-115">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="81725-116">Требования</span><span class="sxs-lookup"><span data-stu-id="81725-116">Requirements</span></span>



| <span data-ttu-id="81725-117">Требование</span><span class="sxs-lookup"><span data-stu-id="81725-117">Requirement</span></span> | <span data-ttu-id="81725-118">Значение</span><span class="sxs-lookup"><span data-stu-id="81725-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="81725-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="81725-119">Minimum supported client</span></span><br/> | <span data-ttu-id="81725-120">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="81725-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                     |
| <span data-ttu-id="81725-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="81725-121">Minimum supported server</span></span><br/> | <span data-ttu-id="81725-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="81725-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="81725-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="81725-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="81725-124"><dt>Н/Д</dt></span><span class="sxs-lookup"><span data-stu-id="81725-124"><dt>N/A</dt></span></span> </dl> |
| <span data-ttu-id="81725-125">IDL</span><span class="sxs-lookup"><span data-stu-id="81725-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="81725-126"><dt>Н/Д</dt></span><span class="sxs-lookup"><span data-stu-id="81725-126"><dt>N/A</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81725-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="81725-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81725-128">**\_аргументы инициализации \_ ОРПК**</span><span class="sxs-lookup"><span data-stu-id="81725-128">**ORPC\_INIT\_ARGS**</span></span>](orpc-init-args.md)
</dt> <dt>

[<span data-ttu-id="81725-129">**дллдебугобжектрпчук**</span><span class="sxs-lookup"><span data-stu-id="81725-129">**DllDebugObjectRPCHook**</span></span>](dlldebugobjectrpchook.md)
</dt> <dt>

[<span data-ttu-id="81725-130">**иорпкдебугнотифи**</span><span class="sxs-lookup"><span data-stu-id="81725-130">**IOrpcDebugNotify**</span></span>](iorpcdebugnotify.md)
</dt> </dl>

 

