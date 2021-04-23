---
description: Проверяет, соответствует ли регион носителя в DVD-дисководе региону DVD-дисковода.
ms.assetid: 864de493-94c2-4f32-96a8-14cfea13dbef
title: Функция Двдлаунчер
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DvdLauncher
api_type:
- DllExport
api_location:
- StorProp.dll
ms.openlocfilehash: ef49be579052e5a9fd493f5bf246a2efbd217c34
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142214"
---
# <a name="dvdlauncher-function"></a><span data-ttu-id="c7448-103">Функция Двдлаунчер</span><span class="sxs-lookup"><span data-stu-id="c7448-103">DvdLauncher function</span></span>

<span data-ttu-id="c7448-104">Проверяет, соответствует ли регион носителя в DVD-дисководе региону DVD-дисковода.</span><span class="sxs-lookup"><span data-stu-id="c7448-104">Verifies that the media region in the DVD drive matches the DVD drive region.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7448-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c7448-105">Syntax</span></span>


```C++
BOOL WINAPI DvdLauncher(
  _In_ HWND HWnd,
  _In_ CHAR DriveLetter
);
```



## <a name="parameters"></a><span data-ttu-id="c7448-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c7448-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7448-107">*HWND* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c7448-107">*HWnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7448-108">Маркер окна верхнего уровня, используемый для любого требуемого пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="c7448-108">A handle to the top-level window to be used for any required user interface.</span></span>

</dd> <dt>

<span data-ttu-id="c7448-109">*Буква_диска* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c7448-109">*DriveLetter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7448-110">Буква диска.</span><span class="sxs-lookup"><span data-stu-id="c7448-110">The drive letter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7448-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c7448-111">Return value</span></span>

<span data-ttu-id="c7448-112">Если функция выполнена удачно и области совпадают, возвращаемое значение не равно нулю.</span><span class="sxs-lookup"><span data-stu-id="c7448-112">If the function succeeds and the regions match, the return value is nonzero.</span></span> <span data-ttu-id="c7448-113">В противном случае возвращаемое значение равно нулю.</span><span class="sxs-lookup"><span data-stu-id="c7448-113">Otherwise, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="c7448-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c7448-114">Remarks</span></span>

<span data-ttu-id="c7448-115">Эта функция не имеет связанной библиотеки импорта.</span><span class="sxs-lookup"><span data-stu-id="c7448-115">This function has no associated import library.</span></span> <span data-ttu-id="c7448-116">Для динамической привязки к StorProp.dll необходимо использовать функции [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="c7448-116">You must use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to StorProp.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7448-117">Требования</span><span class="sxs-lookup"><span data-stu-id="c7448-117">Requirements</span></span>



| <span data-ttu-id="c7448-118">Требование</span><span class="sxs-lookup"><span data-stu-id="c7448-118">Requirement</span></span> | <span data-ttu-id="c7448-119">Значение</span><span class="sxs-lookup"><span data-stu-id="c7448-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c7448-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c7448-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c7448-121">Windows XP</span><span class="sxs-lookup"><span data-stu-id="c7448-121">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="c7448-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c7448-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c7448-123">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c7448-123">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="c7448-124">DLL</span><span class="sxs-lookup"><span data-stu-id="c7448-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c7448-125"><dt>StorProp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c7448-125"><dt>StorProp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7448-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c7448-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7448-127">Функции управления устройствами</span><span class="sxs-lookup"><span data-stu-id="c7448-127">Device Management Functions</span></span>](device-management-functions.md)
</dt> </dl>

 

