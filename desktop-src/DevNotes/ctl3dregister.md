---
description: Регистрирует приложение в качестве клиента CTL3D сегодня.
ms.assetid: 38a4a04a-6322-4eb8-b272-ae9b90f84e0f
title: Функция Ctl3dRegister
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dRegister
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: 4b855c162d9d5f1c43a15d1ebd7219da6f847f37
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648971"
---
# <a name="ctl3dregister-function"></a><span data-ttu-id="3b5fa-103">Функция Ctl3dRegister</span><span class="sxs-lookup"><span data-stu-id="3b5fa-103">Ctl3dRegister function</span></span>

<span data-ttu-id="3b5fa-104">Регистрирует приложение в качестве клиента CTL3D сегодня.</span><span class="sxs-lookup"><span data-stu-id="3b5fa-104">Registers an application as a client of CTL3D.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b5fa-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3b5fa-105">Syntax</span></span>


```C++
BOOL Ctl3dRegister(
   HANDLE hinstApp
);
```



## <a name="parameters"></a><span data-ttu-id="3b5fa-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3b5fa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b5fa-107">*хинстапп*</span><span class="sxs-lookup"><span data-stu-id="3b5fa-107">*hinstApp*</span></span> 
</dt> <dd>

<span data-ttu-id="3b5fa-108">Описатель приложения, регистрируемого в качестве клиента.</span><span class="sxs-lookup"><span data-stu-id="3b5fa-108">A handle to the application to be registered as a client.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b5fa-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3b5fa-109">Return value</span></span>

<span data-ttu-id="3b5fa-110">Возвращает **значение true** , если трехмерные эффекты активны; в противном случае возвращается **значение false**.</span><span class="sxs-lookup"><span data-stu-id="3b5fa-110">Returns **TRUE** if 3D effects are active; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b5fa-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3b5fa-111">Remarks</span></span>

<span data-ttu-id="3b5fa-112">Приложение, использующее CTL3D сегодня, должно вызывать эту функцию в WinMain.</span><span class="sxs-lookup"><span data-stu-id="3b5fa-112">An application that uses CTL3D should call this function in WinMain.</span></span>

<span data-ttu-id="3b5fa-113">Объемные эффекты недоступны в системах, которые имеют меньшее разрешение VGA.</span><span class="sxs-lookup"><span data-stu-id="3b5fa-113">3D effects are not available on systems that have less than VGA resolution.</span></span>

<span data-ttu-id="3b5fa-114">Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="3b5fa-114">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b5fa-115">Требования</span><span class="sxs-lookup"><span data-stu-id="3b5fa-115">Requirements</span></span>



| <span data-ttu-id="3b5fa-116">Требование</span><span class="sxs-lookup"><span data-stu-id="3b5fa-116">Requirement</span></span> | <span data-ttu-id="3b5fa-117">Значение</span><span class="sxs-lookup"><span data-stu-id="3b5fa-117">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3b5fa-118">DLL</span><span class="sxs-lookup"><span data-stu-id="3b5fa-118">DLL</span></span><br/> | <dl> <span data-ttu-id="3b5fa-119"><dt>Ctl3d32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3b5fa-119"><dt>Ctl3d32.dll</dt></span></span> </dl> |



 

 
