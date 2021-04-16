---
description: Закрывает маркер поиска.
ms.assetid: 2e6a547f-26a7-401a-b1e4-3f085ce82729
title: Функция Кскфиндклосе
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSCFindClose
api_type:
- DllExport
api_location:
- Cscmig.dll
ms.openlocfilehash: 69e3ea972ccd67a1db999c186709ef3aeff84be9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657770"
---
# <a name="cscfindclose-function"></a><span data-ttu-id="743ba-103">Функция Кскфиндклосе</span><span class="sxs-lookup"><span data-stu-id="743ba-103">CSCFindClose function</span></span>

<span data-ttu-id="743ba-104">\[Эта функция не поддерживается и не должна использоваться.\]</span><span class="sxs-lookup"><span data-stu-id="743ba-104">\[This function is not supported and should not be used.\]</span></span>

<span data-ttu-id="743ba-105">Закрывает маркер поиска.</span><span class="sxs-lookup"><span data-stu-id="743ba-105">Closes a search handle.</span></span>

## <a name="syntax"></a><span data-ttu-id="743ba-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="743ba-106">Syntax</span></span>


```C++
BOOL WINAPI CSCFindClose(
  _In_ HANDLE hFind
);
```



## <a name="parameters"></a><span data-ttu-id="743ba-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="743ba-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="743ba-108">*хфинд* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="743ba-108">*hFind* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="743ba-109">Маркер поиска, возвращаемый функцией [**кскфиндфирстфилев**](cscfindfirstfilew.md) .</span><span class="sxs-lookup"><span data-stu-id="743ba-109">A search handle returned by the [**CSCFindFirstFileW**](cscfindfirstfilew.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="743ba-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="743ba-110">Return value</span></span>

<span data-ttu-id="743ba-111">Эта функция возвращает **значение true** , если она выполнена. в противном случае возвращается **значение false**.</span><span class="sxs-lookup"><span data-stu-id="743ba-111">This function returns **TRUE** if it succeeds; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="743ba-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="743ba-112">Remarks</span></span>

<span data-ttu-id="743ba-113">Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="743ba-113">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="743ba-114">Требования</span><span class="sxs-lookup"><span data-stu-id="743ba-114">Requirements</span></span>



| <span data-ttu-id="743ba-115">Требование</span><span class="sxs-lookup"><span data-stu-id="743ba-115">Requirement</span></span> | <span data-ttu-id="743ba-116">Значение</span><span class="sxs-lookup"><span data-stu-id="743ba-116">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="743ba-117">DLL</span><span class="sxs-lookup"><span data-stu-id="743ba-117">DLL</span></span><br/> | <dl> <span data-ttu-id="743ba-118"><dt>Cscmig.dll</dt></span><span class="sxs-lookup"><span data-stu-id="743ba-118"><dt>Cscmig.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="743ba-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="743ba-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="743ba-120">**кскфиндфирстфилев**</span><span class="sxs-lookup"><span data-stu-id="743ba-120">**CSCFindFirstFileW**</span></span>](cscfindfirstfilew.md)
</dt> </dl>

 

 
