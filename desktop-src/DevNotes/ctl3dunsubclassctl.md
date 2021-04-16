---
description: Отключает подкласс для указанного элемента управления.
ms.assetid: d4d34624-7d85-4c53-8318-b3e5d6f95f7a
title: Функция Ctl3dUnsubclassCtl
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dUnsubclassCtl
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: ec62c2ecab6d8c90a9c9b7b2570bf5d76afd0589
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648993"
---
# <a name="ctl3dunsubclassctl-function"></a><span data-ttu-id="f371b-103">Функция Ctl3dUnsubclassCtl</span><span class="sxs-lookup"><span data-stu-id="f371b-103">Ctl3dUnsubclassCtl function</span></span>

<span data-ttu-id="f371b-104">Отключает подкласс для указанного элемента управления.</span><span class="sxs-lookup"><span data-stu-id="f371b-104">Turns off subclassing for the specified control.</span></span>

## <a name="syntax"></a><span data-ttu-id="f371b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f371b-105">Syntax</span></span>


```C++
BOOL WINAPI Ctl3dUnsubclassCtl(
   HWND hwnd
);
```



## <a name="parameters"></a><span data-ttu-id="f371b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f371b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f371b-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="f371b-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="f371b-108">Маркер окна управления.</span><span class="sxs-lookup"><span data-stu-id="f371b-108">A handle to the control window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f371b-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f371b-109">Return value</span></span>

<span data-ttu-id="f371b-110">Возвращает **значение true** , если элемент управления успешно подклассаен; в противном случае возвращается **значение false**.</span><span class="sxs-lookup"><span data-stu-id="f371b-110">Returns **TRUE** if the control is successfully subclassed; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="f371b-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f371b-111">Remarks</span></span>

<span data-ttu-id="f371b-112">Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="f371b-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="f371b-113">Требования</span><span class="sxs-lookup"><span data-stu-id="f371b-113">Requirements</span></span>



| <span data-ttu-id="f371b-114">Требование</span><span class="sxs-lookup"><span data-stu-id="f371b-114">Requirement</span></span> | <span data-ttu-id="f371b-115">Значение</span><span class="sxs-lookup"><span data-stu-id="f371b-115">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f371b-116">DLL</span><span class="sxs-lookup"><span data-stu-id="f371b-116">DLL</span></span><br/> | <dl> <span data-ttu-id="f371b-117"><dt>Ctl3d32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f371b-117"><dt>Ctl3d32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f371b-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f371b-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f371b-119">**Ctl3dSubclassCtl**</span><span class="sxs-lookup"><span data-stu-id="f371b-119">**Ctl3dSubclassCtl**</span></span>](ctl3dsubclassctl.md)
</dt> </dl>

 

 
