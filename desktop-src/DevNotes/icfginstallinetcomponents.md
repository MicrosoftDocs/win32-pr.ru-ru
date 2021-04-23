---
description: Устанавливает указанные системные компоненты.
ms.assetid: f4b7b8e5-b392-4208-9f56-b343974e05ff
title: Функция Икфгинсталлинеткомпонентс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IcfgInstallInetComponents
api_type:
- DllExport
api_location:
- Icfgnt5.dll
ms.openlocfilehash: 649b1fa73bcdd83d7fc01d5a4df9a198168a3f1d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648701"
---
# <a name="icfginstallinetcomponents-function"></a><span data-ttu-id="44d99-103">Функция Икфгинсталлинеткомпонентс</span><span class="sxs-lookup"><span data-stu-id="44d99-103">IcfgInstallInetComponents function</span></span>

<span data-ttu-id="44d99-104">Устанавливает указанные системные компоненты.</span><span class="sxs-lookup"><span data-stu-id="44d99-104">Installs the system components specified.</span></span>

## <a name="syntax"></a><span data-ttu-id="44d99-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="44d99-105">Syntax</span></span>


```C++
HRESULT IcfgInstallInetComponents(
   HWND   hwndParent,
   DWORD  dwfOptions,
   LPBOOL lpfNeedsRestart
);
```



## <a name="parameters"></a><span data-ttu-id="44d99-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="44d99-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44d99-107">*хвндпарент*</span><span class="sxs-lookup"><span data-stu-id="44d99-107">*hwndParent*</span></span> 
</dt> <dd>

<span data-ttu-id="44d99-108">Маркер родительского окна.</span><span class="sxs-lookup"><span data-stu-id="44d99-108">A handle to the parent window.</span></span>

</dd> <dt>

<span data-ttu-id="44d99-109">*двфоптионс*</span><span class="sxs-lookup"><span data-stu-id="44d99-109">*dwfOptions*</span></span> 
</dt> <dd>

<span data-ttu-id="44d99-110">Сочетание следующих флагов, управляющих установкой и настройкой.</span><span class="sxs-lookup"><span data-stu-id="44d99-110">A combination of the following flags that control the installation and configuration.</span></span>



| <span data-ttu-id="44d99-111">Значение</span><span class="sxs-lookup"><span data-stu-id="44d99-111">Value</span></span>                                                                                                                                                                                                                                  | <span data-ttu-id="44d99-112">Значение</span><span class="sxs-lookup"><span data-stu-id="44d99-112">Meaning</span></span>                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <span id="ICFG_INSTALLMAIL"></span><span id="icfg_installmail"></span><dl> <span data-ttu-id="44d99-113"><dt>**Икфг \_ ИНСТАЛЛМАИЛ**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="44d99-113"><dt>**ICFG\_INSTALLMAIL**</dt> <dt>0x00000004</dt></span></span> </dl> | <span data-ttu-id="44d99-114">Установите Exchange и Internet Mail.</span><span class="sxs-lookup"><span data-stu-id="44d99-114">Install Exchange and Internet mail.</span></span><br/> |
| <span id="ICFG_INSTALLRAS"></span><span id="icfg_installras"></span><dl> <span data-ttu-id="44d99-115"><dt>**Икфг \_ ИНСТАЛЛРАС**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="44d99-115"><dt>**ICFG\_INSTALLRAS**</dt> <dt>0x00000002</dt></span></span> </dl>    | <span data-ttu-id="44d99-116">Установите RAS (при необходимости).</span><span class="sxs-lookup"><span data-stu-id="44d99-116">Install RAS (if needed).</span></span><br/>            |
| <span id="ICFG_INSTALLTCP"></span><span id="icfg_installtcp"></span><dl> <span data-ttu-id="44d99-117"><dt>**Икфг \_ ИНСТАЛЛТКП**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="44d99-117"><dt>**ICFG\_INSTALLTCP**</dt> <dt>0x00000001</dt></span></span> </dl>    | <span data-ttu-id="44d99-118">Установите TCP/IP (при необходимости).</span><span class="sxs-lookup"><span data-stu-id="44d99-118">Install TCP/IP (if needed).</span></span><br/>         |



 

</dd> <dt>

<span data-ttu-id="44d99-119">*лпфнидсрестарт*</span><span class="sxs-lookup"><span data-stu-id="44d99-119">*lpfNeedsRestart*</span></span> 
</dt> <dd>

<span data-ttu-id="44d99-120">Если это значение не **равно NULL**, то при возврате произойдет **значение true** , только если для завершения установки необходимо перезапустить Windows.</span><span class="sxs-lookup"><span data-stu-id="44d99-120">If this value is non-**NULL**, on return it will be **TRUE** only if Windows must be restarted to complete the installation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44d99-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="44d99-121">Return value</span></span>

<span data-ttu-id="44d99-122">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="44d99-122">Returns an **HRESULT** value.</span></span> <span data-ttu-id="44d99-123">Если ошибки не возникают, возвращается код **\_ успешного выполнения ошибки** .</span><span class="sxs-lookup"><span data-stu-id="44d99-123">If no errors occur, it returns the **ERROR\_SUCCESS** code.</span></span>

## <a name="remarks"></a><span data-ttu-id="44d99-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="44d99-124">Remarks</span></span>

<span data-ttu-id="44d99-125">Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="44d99-125">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="44d99-126">Требования</span><span class="sxs-lookup"><span data-stu-id="44d99-126">Requirements</span></span>



| <span data-ttu-id="44d99-127">Требование</span><span class="sxs-lookup"><span data-stu-id="44d99-127">Requirement</span></span> | <span data-ttu-id="44d99-128">Значение</span><span class="sxs-lookup"><span data-stu-id="44d99-128">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="44d99-129">DLL</span><span class="sxs-lookup"><span data-stu-id="44d99-129">DLL</span></span><br/> | <dl> <span data-ttu-id="44d99-130"><dt>Icfgnt5.dll</dt></span><span class="sxs-lookup"><span data-stu-id="44d99-130"><dt>Icfgnt5.dll</dt></span></span> </dl> |



 

 
