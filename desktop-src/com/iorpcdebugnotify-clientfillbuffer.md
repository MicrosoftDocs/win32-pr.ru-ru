---
title: Иорпкдебугнотифи Клиентфиллбуффер, метод
description: Отправляет данные из клиентского отладчика в отладчик сервера.
ms.assetid: d575cf34-34a2-4951-a87e-7835b2c5b7a0
keywords:
- COM-метод Клиентфиллбуффер
- Метод Клиентфиллбуффер COM, интерфейс Иорпкдебугнотифи
- Интерфейс Иорпкдебугнотифи COM, метод Клиентфиллбуффер
topic_type:
- apiref
api_name:
- IOrpcDebugNotify.ClientFillBuffer
api_location:
- N/A
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 633f4f0a8a3e135ca60468d24356a3f6e038d062
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803929"
---
# <a name="iorpcdebugnotifyclientfillbuffer-method"></a><span data-ttu-id="f9f91-106">Метод Иорпкдебугнотифи:: Клиентфиллбуффер</span><span class="sxs-lookup"><span data-stu-id="f9f91-106">IOrpcDebugNotify::ClientFillBuffer method</span></span>

<span data-ttu-id="f9f91-107">Отправляет данные из клиентского отладчика в отладчик сервера.</span><span class="sxs-lookup"><span data-stu-id="f9f91-107">Sends data from the client debugger to the server debugger.</span></span>

> [!Note]  
> <span data-ttu-id="f9f91-108">Библиотека импорта, содержащая функцию **клиентфиллбуффер** , не включена в пакет средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="f9f91-108">An import library containing the **ClientFillBuffer** function is not included in the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="f9f91-109">Приложение может использовать функции [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) и [**Ошибка GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) для получения указателя на функцию [**дллдебугобжектрпчук**](dlldebugobjectrpchook.md) из oleaut.dll и предоставления этой функции через интерфейс [**иорпкдебугнотифи**](iorpcdebugnotify.md) .</span><span class="sxs-lookup"><span data-stu-id="f9f91-109">An application can use the [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) and [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) functions to retrieve a function pointer to [**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md) from oleaut.dll and provide this function via the [**IOrpcDebugNotify**](iorpcdebugnotify.md) interface.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="f9f91-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f9f91-110">Syntax</span></span>


```C++
void ClientFillBuffer(
   ORPC_DBG_ALL *lpOrpcDebugAll
);
```



## <a name="parameters"></a><span data-ttu-id="f9f91-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="f9f91-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9f91-112">*лпорпкдебугалл*</span><span class="sxs-lookup"><span data-stu-id="f9f91-112">*lpOrpcDebugAll*</span></span> 
</dt> <dd>

<span data-ttu-id="f9f91-113">Указатель на структуру [**ОРПК \_ dbg \_ ALL**](orpc-dbg-all.md) , содержащую сведения об уведомлении, которые система com RPC передает отладчику.</span><span class="sxs-lookup"><span data-stu-id="f9f91-113">A pointer to a [**ORPC\_DBG\_ALL**](orpc-dbg-all.md) structure that contains notification specific information the COM RPC system passes to the debugger.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9f91-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f9f91-114">Return value</span></span>

<span data-ttu-id="f9f91-115">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="f9f91-115">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9f91-116">Требования</span><span class="sxs-lookup"><span data-stu-id="f9f91-116">Requirements</span></span>



| <span data-ttu-id="f9f91-117">Требование</span><span class="sxs-lookup"><span data-stu-id="f9f91-117">Requirement</span></span> | <span data-ttu-id="f9f91-118">Значение</span><span class="sxs-lookup"><span data-stu-id="f9f91-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="f9f91-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f9f91-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f9f91-120">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f9f91-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                     |
| <span data-ttu-id="f9f91-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f9f91-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f9f91-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f9f91-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="f9f91-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="f9f91-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9f91-124"><dt>Н/Д</dt></span><span class="sxs-lookup"><span data-stu-id="f9f91-124"><dt>N/A</dt></span></span> </dl> |
| <span data-ttu-id="f9f91-125">IDL</span><span class="sxs-lookup"><span data-stu-id="f9f91-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f9f91-126"><dt>Н/Д</dt></span><span class="sxs-lookup"><span data-stu-id="f9f91-126"><dt>N/A</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9f91-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f9f91-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9f91-128">**дллдебугобжектрпчук**</span><span class="sxs-lookup"><span data-stu-id="f9f91-128">**DllDebugObjectRPCHook**</span></span>](dlldebugobjectrpchook.md)
</dt> <dt>

[<span data-ttu-id="f9f91-129">**иорпкдебугнотифи**</span><span class="sxs-lookup"><span data-stu-id="f9f91-129">**IOrpcDebugNotify**</span></span>](iorpcdebugnotify.md)
</dt> </dl>

 

