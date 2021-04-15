---
description: Указывает, является ли текущий пользователь администратором.
ms.assetid: e759a6b9-19c3-4a2e-b8cf-1398037f88ee
title: Функция Псетуписусерадмин
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupIsUserAdmin
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 1c40a69fd682c22e2625a3ba362d11d719cf9cce
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669015"
---
# <a name="psetupisuseradmin-function"></a><span data-ttu-id="03436-103">Функция Псетуписусерадмин</span><span class="sxs-lookup"><span data-stu-id="03436-103">pSetupIsUserAdmin function</span></span>

<span data-ttu-id="03436-104">\[Эта функция недоступна в Windows Vista и Windows Server 2008.\]</span><span class="sxs-lookup"><span data-stu-id="03436-104">\[This function is not available in Windows Vista or Windows Server 2008.\]</span></span>

<span data-ttu-id="03436-105">Указывает, является ли текущий пользователь администратором.</span><span class="sxs-lookup"><span data-stu-id="03436-105">Indicates whether the current user is an administrator.</span></span>

## <a name="syntax"></a><span data-ttu-id="03436-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="03436-106">Syntax</span></span>


```C++
BOOL pSetupIsUserAdmin(void);
```



## <a name="parameters"></a><span data-ttu-id="03436-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="03436-107">Parameters</span></span>

<span data-ttu-id="03436-108">У этой функции нет параметров.</span><span class="sxs-lookup"><span data-stu-id="03436-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="03436-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="03436-109">Return value</span></span>

<span data-ttu-id="03436-110">**Значение true** , если текущий пользователь является администратором; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="03436-110">**TRUE** if the current user is an administrator, otherwise **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="03436-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="03436-111">Remarks</span></span>

<span data-ttu-id="03436-112">Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="03436-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="03436-113">Требования</span><span class="sxs-lookup"><span data-stu-id="03436-113">Requirements</span></span>



| <span data-ttu-id="03436-114">Требование</span><span class="sxs-lookup"><span data-stu-id="03436-114">Requirement</span></span> | <span data-ttu-id="03436-115">Значение</span><span class="sxs-lookup"><span data-stu-id="03436-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="03436-116">DLL</span><span class="sxs-lookup"><span data-stu-id="03436-116">DLL</span></span><br/> | <dl> <span data-ttu-id="03436-117"><dt>Setupapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="03436-117"><dt>Setupapi.dll</dt></span></span> </dl> |



 

 
