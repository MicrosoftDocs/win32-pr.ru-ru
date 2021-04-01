---
description: Выполняет поиск указанного исполняемого файла.
ms.assetid: 32c6b054-7e47-4427-bdfe-6b5066db4ac3
title: Функция Сдбжетматчинжексе
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetMatchingExe
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 9d9c8c8c5e9ba0c55068558698b40c7274929364
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895818"
---
# <a name="sdbgetmatchingexe-function"></a><span data-ttu-id="4cd58-103">Функция Сдбжетматчинжексе</span><span class="sxs-lookup"><span data-stu-id="4cd58-103">SdbGetMatchingExe function</span></span>

<span data-ttu-id="4cd58-104">Выполняет поиск указанного исполняемого файла.</span><span class="sxs-lookup"><span data-stu-id="4cd58-104">Searches for the specified executable.</span></span>

## <a name="syntax"></a><span data-ttu-id="4cd58-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4cd58-105">Syntax</span></span>


```C++
BOOL WINAPI SdbGetMatchingExe(
  _In_opt_ HSDB            hSDB,
  _In_     LPCTSTR         szPath,
  _In_opt_ LPCTSTR         szModuleName,
  _In_opt_ LPCTSTR         pszEnvironment,
  _In_     DWORD           dwFlags,
  _Out_    PSDBQUERYRESULT pQueryResult
);
```



## <a name="parameters"></a><span data-ttu-id="4cd58-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4cd58-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4cd58-107">*хсдб* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="4cd58-107">*hSDB* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4cd58-108">Маркер базы данных оболочек совместимости, возвращаемый функцией [**сдбинитдатабасе**](sdbinitdatabase.md) .</span><span class="sxs-lookup"><span data-stu-id="4cd58-108">A handle to the shim database returned by the [**SdbInitDatabase**](sdbinitdatabase.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="4cd58-109">*сзпас* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4cd58-109">*szPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4cd58-110">Путь к исполняемому файлу.</span><span class="sxs-lookup"><span data-stu-id="4cd58-110">The path of the executable.</span></span>

</dd> <dt>

<span data-ttu-id="4cd58-111">*сзмодуленаме* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="4cd58-111">*szModuleName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4cd58-112">Имя модуля.</span><span class="sxs-lookup"><span data-stu-id="4cd58-112">The module name.</span></span>

</dd> <dt>

<span data-ttu-id="4cd58-113">*псзенвиронмент* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="4cd58-113">*pszEnvironment* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4cd58-114">Переменные среды, используемые в качестве контекста поиска.</span><span class="sxs-lookup"><span data-stu-id="4cd58-114">The environment variables to be used as search context.</span></span>

</dd> <dt>

<span data-ttu-id="4cd58-115">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4cd58-115">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4cd58-116">Этот параметр может иметь значение 0 или **сдбгмеф \_ игнорировать \_ окружение** (0x1).</span><span class="sxs-lookup"><span data-stu-id="4cd58-116">This parameter can be 0 or **SDBGMEF\_IGNORE\_ENVIRONMENT** (0x1).</span></span>

</dd> <dt>

<span data-ttu-id="4cd58-117">*пкуериресулт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="4cd58-117">*pQueryResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4cd58-118">Структура [**сдбкуериресулт**](sdbqueryresult.md) .</span><span class="sxs-lookup"><span data-stu-id="4cd58-118">An [**SDBQUERYRESULT**](sdbqueryresult.md) structure.</span></span> <span data-ttu-id="4cd58-119">Если совпадений не найдено, структура содержит **тагреф \_ null**.</span><span class="sxs-lookup"><span data-stu-id="4cd58-119">If no match is found, the structure contains **TAGREF\_NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4cd58-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4cd58-120">Return value</span></span>

<span data-ttu-id="4cd58-121">Функция возвращает **true** при успешном выполнении или **false** в случае сбоя.</span><span class="sxs-lookup"><span data-stu-id="4cd58-121">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="4cd58-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4cd58-122">Remarks</span></span>

<span data-ttu-id="4cd58-123">Завершив работу с возвращенным [**тагреф**](tagref.md), освободите его с помощью функции [**сдбрелеасематчинжексе**](sdbreleasematchingexe.md) .</span><span class="sxs-lookup"><span data-stu-id="4cd58-123">When you have finished with the returned [**TAGREF**](tagref.md), free it using the [**SdbReleaseMatchingExe**](sdbreleasematchingexe.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="4cd58-124">Требования</span><span class="sxs-lookup"><span data-stu-id="4cd58-124">Requirements</span></span>



| <span data-ttu-id="4cd58-125">Требование</span><span class="sxs-lookup"><span data-stu-id="4cd58-125">Requirement</span></span> | <span data-ttu-id="4cd58-126">Значение</span><span class="sxs-lookup"><span data-stu-id="4cd58-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4cd58-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4cd58-127">Minimum supported client</span></span><br/> | <span data-ttu-id="4cd58-128">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4cd58-128">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="4cd58-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4cd58-129">Minimum supported server</span></span><br/> | <span data-ttu-id="4cd58-130">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4cd58-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="4cd58-131">DLL</span><span class="sxs-lookup"><span data-stu-id="4cd58-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4cd58-132"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4cd58-132"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4cd58-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4cd58-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cd58-134">**сдбинитдатабасе**</span><span class="sxs-lookup"><span data-stu-id="4cd58-134">**SdbInitDatabase**</span></span>](sdbinitdatabase.md)
</dt> <dt>

[<span data-ttu-id="4cd58-135">**сдбрелеасематчинжексе**</span><span class="sxs-lookup"><span data-stu-id="4cd58-135">**SdbReleaseMatchingExe**</span></span>](sdbreleasematchingexe.md)
</dt> </dl>

 

 




