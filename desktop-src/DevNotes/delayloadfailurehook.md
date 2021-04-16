---
description: Возвращает адрес функции обратного вызова при сбое загрузки для указанной библиотеки DLL и процесса.
ms.assetid: db1d34cb-800a-4984-b4a3-d1ce1c6ee86c
title: Функция Делайлоадфаилурехук
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DelayLoadFailureHook
api_type:
- DllExport
api_location:
- kernel32.dll
- API-MS-Win-Core-DelayLoad-l1-1-0.dll
- kernelbase.dll
- mincoredload.dll
- minkernelbase.dll
- API-MS-Win-Core-DelayLoad-l1-1-1.dll
ms.openlocfilehash: f4986b70332a2581580d7e3b274e9d3cdcd96532
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657216"
---
# <a name="delayloadfailurehook-function"></a><span data-ttu-id="ae67b-103">Функция Делайлоадфаилурехук</span><span class="sxs-lookup"><span data-stu-id="ae67b-103">DelayLoadFailureHook function</span></span>

<span data-ttu-id="ae67b-104">Возвращает адрес функции обратного вызова при сбое загрузки для указанной библиотеки DLL и процесса.</span><span class="sxs-lookup"><span data-stu-id="ae67b-104">Returns the address of a delay-load failure callback function for the specified DLL and process.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae67b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ae67b-105">Syntax</span></span>


```C++
FARPROC WINAPI DelayLoadFailureHook(
  _In_ LPCSTR pszDllName,
  _In_ LPCSTR pszProcName
);
```



## <a name="parameters"></a><span data-ttu-id="ae67b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ae67b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae67b-107">*псздллнаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ae67b-107">*pszDllName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae67b-108">Имя библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="ae67b-108">The name of the DLL.</span></span>

</dd> <dt>

<span data-ttu-id="ae67b-109">*псзпрокнаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ae67b-109">*pszProcName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae67b-110">Имя процесса.</span><span class="sxs-lookup"><span data-stu-id="ae67b-110">The name of the process.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae67b-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ae67b-111">Return value</span></span>

<span data-ttu-id="ae67b-112">Адрес функции обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="ae67b-112">The address of the callback function.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae67b-113">Требования</span><span class="sxs-lookup"><span data-stu-id="ae67b-113">Requirements</span></span>



| <span data-ttu-id="ae67b-114">Требование</span><span class="sxs-lookup"><span data-stu-id="ae67b-114">Requirement</span></span> | <span data-ttu-id="ae67b-115">Значение</span><span class="sxs-lookup"><span data-stu-id="ae67b-115">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ae67b-116">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ae67b-116">Library</span></span><br/> | <dl> <span data-ttu-id="ae67b-117"><dt>Kernel32.lib</dt></span><span class="sxs-lookup"><span data-stu-id="ae67b-117"><dt>Kernel32.lib</dt></span></span> </dl> |
| <span data-ttu-id="ae67b-118">DLL</span><span class="sxs-lookup"><span data-stu-id="ae67b-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="ae67b-119"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ae67b-119"><dt>Kernel32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae67b-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ae67b-120">See also</span></span>

<dl> <dt>

<span data-ttu-id="ae67b-121">[Перехватчики ошибки](https://msdn.microsoft.com/library/sfcfb0a3(v=VS.71).aspx)</span><span class="sxs-lookup"><span data-stu-id="ae67b-121">[Failure Hooks](https://msdn.microsoft.com/library/sfcfb0a3(v=VS.71).aspx)</span></span>
</dt> </dl>

 

 




