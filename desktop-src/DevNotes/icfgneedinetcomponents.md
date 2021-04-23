---
description: Определяет, установлены ли компоненты, отмеченные в параметрах, в системе.
ms.assetid: 5fda917a-9c4b-42a3-8f79-9c609f56eb9f
title: Функция Икфгнидинеткомпонентс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IcfgNeedInetComponents
api_type:
- DllExport
api_location:
- Icfgnt5.dll
ms.openlocfilehash: c851ed7d5610d96af636afb60114a51be9c711f4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657741"
---
# <a name="icfgneedinetcomponents-function"></a><span data-ttu-id="11f35-103">Функция Икфгнидинеткомпонентс</span><span class="sxs-lookup"><span data-stu-id="11f35-103">IcfgNeedInetComponents function</span></span>

<span data-ttu-id="11f35-104">Определяет, установлены ли компоненты, отмеченные в параметрах, в системе.</span><span class="sxs-lookup"><span data-stu-id="11f35-104">Determines whether components marked in the options are installed on the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="11f35-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="11f35-105">Syntax</span></span>


```C++
HRESULT IcfgNeedInetComponents(
   DWORD  dwfOptions,
   LPBOOL lpfNeedComponents
);
```



## <a name="parameters"></a><span data-ttu-id="11f35-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="11f35-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11f35-107">*двфоптионс*</span><span class="sxs-lookup"><span data-stu-id="11f35-107">*dwfOptions*</span></span> 
</dt> <dd>

<span data-ttu-id="11f35-108">Сочетание следующих флагов, указывающих, какие компоненты следует обнаружить из следующего списка.</span><span class="sxs-lookup"><span data-stu-id="11f35-108">A combination of the following flags that specify which components to detect from the following list.</span></span>



| <span data-ttu-id="11f35-109">Значение</span><span class="sxs-lookup"><span data-stu-id="11f35-109">Value</span></span>                                                                                                                                                                                                                                  | <span data-ttu-id="11f35-110">Значение</span><span class="sxs-lookup"><span data-stu-id="11f35-110">Meaning</span></span>                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <span id="ICFG_INSTALLMAIL"></span><span id="icfg_installmail"></span><dl> <span data-ttu-id="11f35-111"><dt>**Икфг \_ ИНСТАЛЛМАИЛ**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="11f35-111"><dt>**ICFG\_INSTALLMAIL**</dt> <dt>0x00000004</dt></span></span> </dl> | <span data-ttu-id="11f35-112">Требуется ли Exchange или Internet Mail?</span><span class="sxs-lookup"><span data-stu-id="11f35-112">Is Exchange or Internet mail needed?</span></span><br/> |
| <span id="ICFG_INSTALLRAS"></span><span id="icfg_installras"></span><dl> <span data-ttu-id="11f35-113"><dt>**Икфг \_ ИНСТАЛЛРАС**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="11f35-113"><dt>**ICFG\_INSTALLRAS**</dt> <dt>0x00000002</dt></span></span> </dl>    | <span data-ttu-id="11f35-114">Требуется ли RAS?</span><span class="sxs-lookup"><span data-stu-id="11f35-114">Is RAS needed?</span></span><br/>                       |
| <span id="ICFG_INSTALLTCP"></span><span id="icfg_installtcp"></span><dl> <span data-ttu-id="11f35-115"><dt>**Икфг \_ ИНСТАЛЛТКП**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="11f35-115"><dt>**ICFG\_INSTALLTCP**</dt> <dt>0x00000001</dt></span></span> </dl>    | <span data-ttu-id="11f35-116">Требуется ли TCP/IP?</span><span class="sxs-lookup"><span data-stu-id="11f35-116">Is TCP/IP needed?</span></span><br/>                    |



 

</dd> <dt>

<span data-ttu-id="11f35-117">*лпфнидкомпонентс*</span><span class="sxs-lookup"><span data-stu-id="11f35-117">*lpfNeedComponents*</span></span> 
</dt> <dd>

<span data-ttu-id="11f35-118">Если это значение не **равно NULL**, возвращается **значение true** , если один или несколько компонентов не установлены в системе.</span><span class="sxs-lookup"><span data-stu-id="11f35-118">If this value is non-**NULL**, it is **TRUE** on return if one or more components are not installed on the system.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11f35-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="11f35-119">Return value</span></span>

<span data-ttu-id="11f35-120">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="11f35-120">Returns an **HRESULT** value.</span></span> <span data-ttu-id="11f35-121">Если ошибки не возникают, возвращается код **\_ успешного выполнения ошибки** .</span><span class="sxs-lookup"><span data-stu-id="11f35-121">If no errors occur, it returns the **ERROR\_SUCCESS** code.</span></span>

## <a name="remarks"></a><span data-ttu-id="11f35-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="11f35-122">Remarks</span></span>

<span data-ttu-id="11f35-123">Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="11f35-123">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="11f35-124">Требования</span><span class="sxs-lookup"><span data-stu-id="11f35-124">Requirements</span></span>



| <span data-ttu-id="11f35-125">Требование</span><span class="sxs-lookup"><span data-stu-id="11f35-125">Requirement</span></span> | <span data-ttu-id="11f35-126">Значение</span><span class="sxs-lookup"><span data-stu-id="11f35-126">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="11f35-127">DLL</span><span class="sxs-lookup"><span data-stu-id="11f35-127">DLL</span></span><br/> | <dl> <span data-ttu-id="11f35-128"><dt>Icfgnt5.dll</dt></span><span class="sxs-lookup"><span data-stu-id="11f35-128"><dt>Icfgnt5.dll</dt></span></span> </dl> |



 

 
