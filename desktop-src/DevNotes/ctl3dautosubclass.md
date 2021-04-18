---
description: Автоматически подклассы и добавляют трехмерные эффекты во все диалоговые окна приложения.
ms.assetid: 96555052-c564-4cc7-9b24-e527f8e2f879
title: Функция Ctl3dAutoSubclass
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dAutoSubclass
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: 85f4c85d1d608ff97147a935806b090162f5a78a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649017"
---
# <a name="ctl3dautosubclass-function"></a><span data-ttu-id="4522b-103">Функция Ctl3dAutoSubclass</span><span class="sxs-lookup"><span data-stu-id="4522b-103">Ctl3dAutoSubclass function</span></span>

<span data-ttu-id="4522b-104">Автоматически подклассы и добавляют трехмерные эффекты во все диалоговые окна приложения.</span><span class="sxs-lookup"><span data-stu-id="4522b-104">Automatically subclasses and adds 3D effects to all dialog boxes in the application.</span></span>

## <a name="syntax"></a><span data-ttu-id="4522b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4522b-105">Syntax</span></span>


```C++
PUBLIC BOOL FAR PASCAL Ctl3dAutoSubclass(
   HANDLE hinstApp
);
```



## <a name="parameters"></a><span data-ttu-id="4522b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4522b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4522b-107">*хинстапп*</span><span class="sxs-lookup"><span data-stu-id="4522b-107">*hinstApp*</span></span> 
</dt> <dd>

<span data-ttu-id="4522b-108">Описатель приложения, регистрируемого в качестве клиента.</span><span class="sxs-lookup"><span data-stu-id="4522b-108">A handle to the application to be registered as a client.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4522b-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4522b-109">Return value</span></span>

<span data-ttu-id="4522b-110">Возвращает **значение true** , если не существует одно из следующих условий. в этом случае возвращается **значение false**:</span><span class="sxs-lookup"><span data-stu-id="4522b-110">Returns **TRUE** unless one of the following conditions exists, in which case it returns **FALSE**:</span></span>

-   <span data-ttu-id="4522b-111">CTL3D сегодня работает под управлением Windows версии 3,0 или более ранней.</span><span class="sxs-lookup"><span data-stu-id="4522b-111">CTL3D is running under Windows version 3.0 or earlier.</span></span>
-   <span data-ttu-id="4522b-112">CTL3D сегодня не имеет свободного места в таблицах для текущего приложения.</span><span class="sxs-lookup"><span data-stu-id="4522b-112">CTL3D does not have space available in its tables for the current application.</span></span> <span data-ttu-id="4522b-113">CTL3D сегодня может обслуживать до 32 приложений одновременно.</span><span class="sxs-lookup"><span data-stu-id="4522b-113">CTL3D can service up to 32 applications at the same time.</span></span>
-   <span data-ttu-id="4522b-114">CTL3D сегодня не может установить свой обработчик CBT.</span><span class="sxs-lookup"><span data-stu-id="4522b-114">CTL3D cannot install its CBT hook.</span></span>

## <a name="remarks"></a><span data-ttu-id="4522b-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4522b-115">Remarks</span></span>

<span data-ttu-id="4522b-116">Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="4522b-116">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="4522b-117">Требования</span><span class="sxs-lookup"><span data-stu-id="4522b-117">Requirements</span></span>



| <span data-ttu-id="4522b-118">Требование</span><span class="sxs-lookup"><span data-stu-id="4522b-118">Requirement</span></span> | <span data-ttu-id="4522b-119">Значение</span><span class="sxs-lookup"><span data-stu-id="4522b-119">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4522b-120">DLL</span><span class="sxs-lookup"><span data-stu-id="4522b-120">DLL</span></span><br/> | <dl> <span data-ttu-id="4522b-121"><dt>Ctl3d32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4522b-121"><dt>Ctl3d32.dll</dt></span></span> </dl> |



 

 
