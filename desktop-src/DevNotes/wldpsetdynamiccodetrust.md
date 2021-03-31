---
description: Задает для .NET динамический код .NET CRL на диске.
ms.assetid: 4C8C3EF5-5C3C-4710-8223-D7B5BA86EF47
title: Функция Влдпсетдинамиккодетруст (Wldp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WldpSetDynamicCodeTrust
api_type:
- DllExport
api_location:
- wldp.dll
ms.openlocfilehash: a266563b40d255fe9e904f02e4e4593d4c4d3f33
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423290"
---
# <a name="wldpsetdynamiccodetrust-function"></a><span data-ttu-id="601ca-103">Функция Влдпсетдинамиккодетруст</span><span class="sxs-lookup"><span data-stu-id="601ca-103">WldpSetDynamicCodeTrust function</span></span>

<span data-ttu-id="601ca-104">Задает для .NET динамический код .NET CRL на диске.</span><span class="sxs-lookup"><span data-stu-id="601ca-104">Sets an on-disk .NET CRL Dynamic Code trustable for .NET.</span></span>

## <a name="syntax"></a><span data-ttu-id="601ca-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="601ca-105">Syntax</span></span>


```C++
HRESULT WINAPI WldpSetDynamicCodeTrust(
   HANDLE FileHandle
);
```



## <a name="parameters"></a><span data-ttu-id="601ca-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="601ca-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="601ca-107">*FileHandle*</span><span class="sxs-lookup"><span data-stu-id="601ca-107">*FileHandle*</span></span> 
</dt> <dd>

<span data-ttu-id="601ca-108">Обработайте файл динамического кода на диске.</span><span class="sxs-lookup"><span data-stu-id="601ca-108">Handle to a on-disk dynamic code file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="601ca-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="601ca-109">Return value</span></span>

<span data-ttu-id="601ca-110">Этот метод возвращает **значение \_ ОК** в случае успеха или код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="601ca-110">This method returns **S\_OK** if successful or a failure code otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="601ca-111">Требования</span><span class="sxs-lookup"><span data-stu-id="601ca-111">Requirements</span></span>



| <span data-ttu-id="601ca-112">Требование</span><span class="sxs-lookup"><span data-stu-id="601ca-112">Requirement</span></span> | <span data-ttu-id="601ca-113">Значение</span><span class="sxs-lookup"><span data-stu-id="601ca-113">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="601ca-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="601ca-114">Minimum supported client</span></span><br/> | <span data-ttu-id="601ca-115">\[Только для настольных приложений Windows 10 версии 1803\]</span><span class="sxs-lookup"><span data-stu-id="601ca-115">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="601ca-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="601ca-116">Minimum supported server</span></span><br/> | <span data-ttu-id="601ca-117">\[Только для настольных приложений Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="601ca-117">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="601ca-118">Header</span><span class="sxs-lookup"><span data-stu-id="601ca-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="601ca-119"><dt>Wldp. h</dt></span><span class="sxs-lookup"><span data-stu-id="601ca-119"><dt>Wldp.h</dt></span></span> </dl>   |
| <span data-ttu-id="601ca-120">DLL</span><span class="sxs-lookup"><span data-stu-id="601ca-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="601ca-121"><dt>Wldp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="601ca-121"><dt>Wldp.dll</dt></span></span> </dl> |



 

 




