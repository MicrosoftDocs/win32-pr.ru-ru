---
description: Находит целевую функцию указанного импорта и заменяет указатель функции в преобразователе импорта на целевой объект реализации функции.
ms.assetid: 4ab79b7c-81d1-40bf-a76b-217d93567e40
title: Функция Ресолведелайлоадедапи
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ResolveDelayLoadedAPI
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-DelayLoad-l1-1-1.dll
- kernelbase.dll
- mincoredload.dll
- minkernelbase.dll
ms.openlocfilehash: 019729cacb45cce87de2cc4015c661c494125108
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668790"
---
# <a name="resolvedelayloadedapi-function"></a><span data-ttu-id="31809-103">Функция Ресолведелайлоадедапи</span><span class="sxs-lookup"><span data-stu-id="31809-103">ResolveDelayLoadedAPI function</span></span>

<span data-ttu-id="31809-104">Находит целевую функцию указанного импорта и заменяет указатель функции в преобразователе импорта на целевой объект реализации функции.</span><span class="sxs-lookup"><span data-stu-id="31809-104">Locates the target function of the specified import and replaces the function pointer in the import thunk with the target of the function implementation.</span></span>

## <a name="syntax"></a><span data-ttu-id="31809-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="31809-105">Syntax</span></span>


```C++
PVOID WINAPI ResolveDelayLoadedAPI(
  _In_       PVOID                             ParentModuleBase,
  _In_       PCIMAGE_DELAYLOAD_DESCRIPTOR      DelayloadDescriptor,
  _In_opt_   PDELAYLOAD_FAILURE_DLL_CALLBACK   FailureDllHook,
  _In_opt_   PDELAYLOAD_FAILURE_SYSTEM_ROUTINE FailureSystemHook,
  _Out_      PIMAGE_THUNK_DATA                 ThunkAddress,
  _Reserved_ ULONG                             Flags
);
```



## <a name="parameters"></a><span data-ttu-id="31809-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="31809-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31809-107">*Парентмодулебасе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="31809-107">*ParentModuleBase* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31809-108">Адрес основания модуля, в котором импортируется функция с отложенной загрузкой.</span><span class="sxs-lookup"><span data-stu-id="31809-108">The address of the base of the module importing a delay-loaded function.</span></span>

</dd> <dt>

<span data-ttu-id="31809-109">*Делайлоаддескриптор* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="31809-109">*DelayloadDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31809-110">Дескриптор загружаемого модуля.</span><span class="sxs-lookup"><span data-stu-id="31809-110">The descriptor for the module to be loaded.</span></span>

</dd> <dt>

<span data-ttu-id="31809-111">*Фаилуредллхук* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="31809-111">*FailureDllHook* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="31809-112">Адрес ловушки сбоя.</span><span class="sxs-lookup"><span data-stu-id="31809-112">The address of the failure hook.</span></span> <span data-ttu-id="31809-113">См. [**делайлоадфаилурехук**](delayloadfailurehook.md).</span><span class="sxs-lookup"><span data-stu-id="31809-113">See [**DelayLoadFailureHook**](delayloadfailurehook.md).</span></span>

</dd> <dt>

<span data-ttu-id="31809-114">*Фаилуресистемхук* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="31809-114">*FailureSystemHook* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="31809-115">Адрес обработчика ошибок системы.</span><span class="sxs-lookup"><span data-stu-id="31809-115">The address of the system failure hook.</span></span>

</dd> <dt>

<span data-ttu-id="31809-116">*Сункаддресс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="31809-116">*ThunkAddress* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="31809-117">Данные преобразователя для целевой функции.</span><span class="sxs-lookup"><span data-stu-id="31809-117">The thunk data for the target function.</span></span> <span data-ttu-id="31809-118">Используется для поиска конкретной записи таблицы имен функции.</span><span class="sxs-lookup"><span data-stu-id="31809-118">Used to find the specific name table entry of the function.</span></span>

</dd> <dt>

<span data-ttu-id="31809-119">*Флаги*</span><span class="sxs-lookup"><span data-stu-id="31809-119">*Flags*</span></span> 
</dt> <dd>

<span data-ttu-id="31809-120">Процессу значение должно быть равно 0.</span><span class="sxs-lookup"><span data-stu-id="31809-120">Reserved; must be 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31809-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="31809-121">Return value</span></span>

<span data-ttu-id="31809-122">Адрес импорта или заглушка сбоя для него.</span><span class="sxs-lookup"><span data-stu-id="31809-122">The address of the import, or the failure stub for it.</span></span>

## <a name="requirements"></a><span data-ttu-id="31809-123">Требования</span><span class="sxs-lookup"><span data-stu-id="31809-123">Requirements</span></span>



| <span data-ttu-id="31809-124">Требование</span><span class="sxs-lookup"><span data-stu-id="31809-124">Requirement</span></span> | <span data-ttu-id="31809-125">Значение</span><span class="sxs-lookup"><span data-stu-id="31809-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="31809-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="31809-126">Library</span></span><br/> | <dl> <span data-ttu-id="31809-127"><dt>Kernel32.lib</dt></span><span class="sxs-lookup"><span data-stu-id="31809-127"><dt>Kernel32.lib</dt></span></span> </dl> |
| <span data-ttu-id="31809-128">DLL</span><span class="sxs-lookup"><span data-stu-id="31809-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="31809-129"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="31809-129"><dt>Kernel32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31809-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="31809-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="31809-131">[Поддержка компоновщика для Delay-Loadedных библиотек DLL](https://msdn.microsoft.com/library/151kt790(v=VS.71).aspx)</span><span class="sxs-lookup"><span data-stu-id="31809-131">[Linker Support for Delay-Loaded DLLs](https://msdn.microsoft.com/library/151kt790(v=VS.71).aspx)</span></span>
</dt> </dl>

 

 




