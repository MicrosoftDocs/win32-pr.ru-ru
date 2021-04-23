---
title: Иорпкдебугнотифи Клиентжетбуфферсизе, метод
description: Извлекает размер буфера RPC из клиентского отладчика.
ms.assetid: 05475156-1508-4eb2-82a6-bb1701839fbd
keywords:
- COM-метод Клиентжетбуфферсизе
- Метод Клиентжетбуфферсизе COM, интерфейс Иорпкдебугнотифи
- Интерфейс Иорпкдебугнотифи COM, метод Клиентжетбуфферсизе
topic_type:
- apiref
api_name:
- IOrpcDebugNotify.ClientGetBufferSize
api_location:
- N/A
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50bd925b9c518c78ca37aa8219a00965f398c415
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672893"
---
# <a name="iorpcdebugnotifyclientgetbuffersize-method"></a><span data-ttu-id="8bb34-106">Метод Иорпкдебугнотифи:: Клиентжетбуфферсизе</span><span class="sxs-lookup"><span data-stu-id="8bb34-106">IOrpcDebugNotify::ClientGetBufferSize method</span></span>

<span data-ttu-id="8bb34-107">Извлекает размер буфера RPC из клиентского отладчика.</span><span class="sxs-lookup"><span data-stu-id="8bb34-107">Retrieves the RPC buffer size from the client-side debugger.</span></span>

> [!Note]  
> <span data-ttu-id="8bb34-108">Библиотека импорта, содержащая функцию **клиентжетбуфферсизе** , не включена в пакет средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="8bb34-108">An import library containing the **ClientGetBufferSize** function is not included in the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="8bb34-109">Приложение может использовать функции [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) и [**Ошибка GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) для получения указателя на функцию [**дллдебугобжектрпчук**](dlldebugobjectrpchook.md) из oleaut.dll и предоставления этой функции через интерфейс [**иорпкдебугнотифи**](iorpcdebugnotify.md) .</span><span class="sxs-lookup"><span data-stu-id="8bb34-109">An application can use the [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) and [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) functions to retrieve a function pointer to [**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md) from oleaut.dll and provide this function via the [**IOrpcDebugNotify**](iorpcdebugnotify.md) interface.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="8bb34-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8bb34-110">Syntax</span></span>


```C++
void ClientGetBufferSize(
   ORPC_DBG_ALL *lpOrpcDebugAll
);
```



## <a name="parameters"></a><span data-ttu-id="8bb34-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="8bb34-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8bb34-112">*лпорпкдебугалл*</span><span class="sxs-lookup"><span data-stu-id="8bb34-112">*lpOrpcDebugAll*</span></span> 
</dt> <dd>

<span data-ttu-id="8bb34-113">Указатель на структуру [**ОРПК \_ dbg \_ ALL**](orpc-dbg-all.md) , содержащую сведения об уведомлении, которые система com RPC передает отладчику.</span><span class="sxs-lookup"><span data-stu-id="8bb34-113">A pointer to a [**ORPC\_DBG\_ALL**](orpc-dbg-all.md) structure that contains notification specific information the COM RPC system passes to the debugger.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8bb34-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8bb34-114">Return value</span></span>

<span data-ttu-id="8bb34-115">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="8bb34-115">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="8bb34-116">Требования</span><span class="sxs-lookup"><span data-stu-id="8bb34-116">Requirements</span></span>



| <span data-ttu-id="8bb34-117">Требование</span><span class="sxs-lookup"><span data-stu-id="8bb34-117">Requirement</span></span> | <span data-ttu-id="8bb34-118">Значение</span><span class="sxs-lookup"><span data-stu-id="8bb34-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="8bb34-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8bb34-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8bb34-120">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8bb34-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                     |
| <span data-ttu-id="8bb34-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8bb34-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8bb34-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8bb34-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="8bb34-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="8bb34-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="8bb34-124"><dt>Н/Д</dt></span><span class="sxs-lookup"><span data-stu-id="8bb34-124"><dt>N/A</dt></span></span> </dl> |
| <span data-ttu-id="8bb34-125">IDL</span><span class="sxs-lookup"><span data-stu-id="8bb34-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8bb34-126"><dt>Н/Д</dt></span><span class="sxs-lookup"><span data-stu-id="8bb34-126"><dt>N/A</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8bb34-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8bb34-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8bb34-128">**\_аргументы инициализации \_ ОРПК**</span><span class="sxs-lookup"><span data-stu-id="8bb34-128">**ORPC\_INIT\_ARGS**</span></span>](orpc-init-args.md)
</dt> <dt>

[<span data-ttu-id="8bb34-129">**дллдебугобжектрпчук**</span><span class="sxs-lookup"><span data-stu-id="8bb34-129">**DllDebugObjectRPCHook**</span></span>](dlldebugobjectrpchook.md)
</dt> <dt>

[<span data-ttu-id="8bb34-130">**иорпкдебугнотифи**</span><span class="sxs-lookup"><span data-stu-id="8bb34-130">**IOrpcDebugNotify**</span></span>](iorpcdebugnotify.md)
</dt> </dl>

 

