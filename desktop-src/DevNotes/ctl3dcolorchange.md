---
description: Обрабатывает изменения системного цвета для приложений, использующих CTL3D сегодня.
ms.assetid: b1eadb7d-39a5-47e9-9ae5-62bd33557f6b
title: Функция Ctl3dColorChange
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dColorChange
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: 7e7b0d4480fde480ea24a6c2c0dd8a7a849fbc75
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657424"
---
# <a name="ctl3dcolorchange-function"></a><span data-ttu-id="bcbb0-103">Функция Ctl3dColorChange</span><span class="sxs-lookup"><span data-stu-id="bcbb0-103">Ctl3dColorChange function</span></span>

<span data-ttu-id="bcbb0-104">Обрабатывает изменения системного цвета для приложений, использующих CTL3D сегодня.</span><span class="sxs-lookup"><span data-stu-id="bcbb0-104">Handles system color changes for applications that use CTL3D.</span></span>

## <a name="syntax"></a><span data-ttu-id="bcbb0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bcbb0-105">Syntax</span></span>


```C++
BOOL Ctl3dColorChange(void);
```



## <a name="parameters"></a><span data-ttu-id="bcbb0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bcbb0-106">Parameters</span></span>

<span data-ttu-id="bcbb0-107">У этой функции нет параметров.</span><span class="sxs-lookup"><span data-stu-id="bcbb0-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bcbb0-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bcbb0-108">Return value</span></span>

<span data-ttu-id="bcbb0-109">Возвращает **значение true** , если функция выполнена. в противном случае возвращается **значение false**.</span><span class="sxs-lookup"><span data-stu-id="bcbb0-109">Returns **TRUE** if the function succeeds; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="bcbb0-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bcbb0-110">Remarks</span></span>

<span data-ttu-id="bcbb0-111">Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="bcbb0-111">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

<span data-ttu-id="bcbb0-112">Эта функция должна вызываться в главном окне приложения для сообщения **WM \_ сисколорчанже** , как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="bcbb0-112">This function should be called in the application's main window procedure for the **WM\_SYSCOLORCHANGE** message, as shown below.</span></span>

## <a name="examples"></a><span data-ttu-id="bcbb0-113">Примеры</span><span class="sxs-lookup"><span data-stu-id="bcbb0-113">Examples</span></span>

``` syntax
case WM_SYSCOLORCHANGE:
   Ctl3dColorChange();
   break;
```

## <a name="requirements"></a><span data-ttu-id="bcbb0-114">Требования</span><span class="sxs-lookup"><span data-stu-id="bcbb0-114">Requirements</span></span>



| <span data-ttu-id="bcbb0-115">Требование</span><span class="sxs-lookup"><span data-stu-id="bcbb0-115">Requirement</span></span> | <span data-ttu-id="bcbb0-116">Значение</span><span class="sxs-lookup"><span data-stu-id="bcbb0-116">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bcbb0-117">DLL</span><span class="sxs-lookup"><span data-stu-id="bcbb0-117">DLL</span></span><br/> | <dl> <span data-ttu-id="bcbb0-118"><dt>Ctl3d32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bcbb0-118"><dt>Ctl3d32.dll</dt></span></span> </dl> |



 

 
