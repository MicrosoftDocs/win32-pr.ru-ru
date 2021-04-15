---
description: Пересылает работу в разрешении импортов с отложенной загрузкой из родительского двоичного файла в целевой двоичный файл.
ms.assetid: 65629d7b-36b0-426b-a20d-ec736b8461dc
title: Функция Ресолведелайлоадсфромдлл
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ResolveDelayLoadsFromDll
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-DelayLoad-l1-1-1.dll
- kernelbase.dll
- mincoredload.dll
- minkernelbase.dll
ms.openlocfilehash: a0fb517de7384a964c21c9e1a0a3e695a0d6e6cc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669295"
---
# <a name="resolvedelayloadsfromdll-function"></a><span data-ttu-id="8f1d5-103">Функция Ресолведелайлоадсфромдлл</span><span class="sxs-lookup"><span data-stu-id="8f1d5-103">ResolveDelayLoadsFromDll function</span></span>

<span data-ttu-id="8f1d5-104">Пересылает работу в разрешении импортов с отложенной загрузкой из родительского двоичного файла в целевой двоичный файл.</span><span class="sxs-lookup"><span data-stu-id="8f1d5-104">Forwards the work in resolving delay-loaded imports from the parent binary to a target binary.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f1d5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8f1d5-105">Syntax</span></span>


```C++
NTSTATUS WINAPI ResolveDelayLoadsFromDll(
  _In_       PVOID  ParentBase,
  _In_       LPCSTR TargetDllName,
  _Reserved_ ULONG  Flags
);
```



## <a name="parameters"></a><span data-ttu-id="8f1d5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8f1d5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f1d5-107">*Парентбасе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8f1d5-107">*ParentBase* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f1d5-108">Базовый адрес модуля, который откладывает загрузку другого двоичного файла.</span><span class="sxs-lookup"><span data-stu-id="8f1d5-108">The base address of the module that delay loads another binary.</span></span>

</dd> <dt>

<span data-ttu-id="8f1d5-109">*Таржетдллнаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8f1d5-109">*TargetDllName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f1d5-110">Имя целевой библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="8f1d5-110">The name of the target DLL.</span></span>

</dd> <dt>

<span data-ttu-id="8f1d5-111">*Флаги*</span><span class="sxs-lookup"><span data-stu-id="8f1d5-111">*Flags*</span></span> 
</dt> <dd>

<span data-ttu-id="8f1d5-112">Процессу значение должно быть равно 0.</span><span class="sxs-lookup"><span data-stu-id="8f1d5-112">Reserved; must be 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f1d5-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8f1d5-113">Return value</span></span>

<span data-ttu-id="8f1d5-114">Адрес дескриптора загрузки с задержкой, если он найден; в противном случае **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="8f1d5-114">The address of the delay-load descriptor, if it is found; otherwise, **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f1d5-115">Требования</span><span class="sxs-lookup"><span data-stu-id="8f1d5-115">Requirements</span></span>



| <span data-ttu-id="8f1d5-116">Требование</span><span class="sxs-lookup"><span data-stu-id="8f1d5-116">Requirement</span></span> | <span data-ttu-id="8f1d5-117">Значение</span><span class="sxs-lookup"><span data-stu-id="8f1d5-117">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8f1d5-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8f1d5-118">Library</span></span><br/> | <dl> <span data-ttu-id="8f1d5-119"><dt>Kernel32.lib</dt></span><span class="sxs-lookup"><span data-stu-id="8f1d5-119"><dt>Kernel32.lib</dt></span></span> </dl> |
| <span data-ttu-id="8f1d5-120">DLL</span><span class="sxs-lookup"><span data-stu-id="8f1d5-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="8f1d5-121"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8f1d5-121"><dt>Kernel32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f1d5-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8f1d5-122">See also</span></span>

<dl> <dt>

<span data-ttu-id="8f1d5-123">[Поддержка компоновщика для Delay-Loadedных библиотек DLL](https://msdn.microsoft.com/library/151kt790(v=VS.71).aspx)</span><span class="sxs-lookup"><span data-stu-id="8f1d5-123">[Linker Support for Delay-Loaded DLLs](https://msdn.microsoft.com/library/151kt790(v=VS.71).aspx)</span></span>
</dt> </dl>

 

 




