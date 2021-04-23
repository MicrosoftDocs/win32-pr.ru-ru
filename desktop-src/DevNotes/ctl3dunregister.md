---
description: Отменяет регистрацию приложения в качестве клиента CTL3D сегодня.
ms.assetid: 21990A79-F90D-4AE1-AB02-2B33583B47F5
title: Функция Ctl3dUnregister
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dUnregister
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: 85cd45062da9c01ef8af5a312a855bfaab6a6bf7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648994"
---
# <a name="ctl3dunregister-function"></a><span data-ttu-id="0ab63-103">Функция Ctl3dUnregister</span><span class="sxs-lookup"><span data-stu-id="0ab63-103">Ctl3dUnregister function</span></span>

<span data-ttu-id="0ab63-104">Отменяет регистрацию приложения в качестве клиента CTL3D сегодня.</span><span class="sxs-lookup"><span data-stu-id="0ab63-104">Unregisters an application as a client of CTL3D.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ab63-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0ab63-105">Syntax</span></span>


```C++
BOOL Ctl3dUnregister(
   HANDLE hinstApp
);
```



## <a name="parameters"></a><span data-ttu-id="0ab63-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0ab63-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ab63-107">*хинстапп*</span><span class="sxs-lookup"><span data-stu-id="0ab63-107">*hinstApp*</span></span> 
</dt> <dd>

<span data-ttu-id="0ab63-108">Маркер для отмены регистрации приложения в качестве клиента.</span><span class="sxs-lookup"><span data-stu-id="0ab63-108">A handle to the application to be unregistered as a client.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ab63-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0ab63-109">Return value</span></span>

<span data-ttu-id="0ab63-110">Возвращает **значение true** , если регистрация приложения в качестве клиента CTL3D сегодня отменена. в противном случае возвращается **значение false**.</span><span class="sxs-lookup"><span data-stu-id="0ab63-110">Returns **TRUE** if the application is unregistered as a client of CTL3D; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="0ab63-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0ab63-111">Remarks</span></span>

<span data-ttu-id="0ab63-112">Приложение, использующее CTL3D сегодня, должно вызывать эту функцию в WinMain.</span><span class="sxs-lookup"><span data-stu-id="0ab63-112">An application that uses CTL3D should call this function in WinMain.</span></span>

<span data-ttu-id="0ab63-113">Объемные эффекты недоступны в системах, которые имеют меньшее разрешение VGA.</span><span class="sxs-lookup"><span data-stu-id="0ab63-113">3D effects are not available on systems that have less than VGA resolution.</span></span>

<span data-ttu-id="0ab63-114">Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="0ab63-114">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ab63-115">Требования</span><span class="sxs-lookup"><span data-stu-id="0ab63-115">Requirements</span></span>



| <span data-ttu-id="0ab63-116">Требование</span><span class="sxs-lookup"><span data-stu-id="0ab63-116">Requirement</span></span> | <span data-ttu-id="0ab63-117">Значение</span><span class="sxs-lookup"><span data-stu-id="0ab63-117">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0ab63-118">DLL</span><span class="sxs-lookup"><span data-stu-id="0ab63-118">DLL</span></span><br/> | <dl> <span data-ttu-id="0ab63-119"><dt>Ctl3d32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0ab63-119"><dt>Ctl3d32.dll</dt></span></span> </dl> |



 

 
