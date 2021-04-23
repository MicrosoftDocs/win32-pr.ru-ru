---
description: Получает системный каталог Апппатч.
ms.assetid: 1c79411f-1f90-4b90-84c7-24a34cf0d91d
title: Функция Сдбжетапппатчдир
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetAppPatchDir
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 60a3b14bcca1be3ecb8d33b0d3f344f08bc11b28
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104140742"
---
# <a name="sdbgetapppatchdir-function"></a><span data-ttu-id="1092e-103">Функция Сдбжетапппатчдир</span><span class="sxs-lookup"><span data-stu-id="1092e-103">SdbGetAppPatchDir function</span></span>

<span data-ttu-id="1092e-104">Получает системный каталог Апппатч.</span><span class="sxs-lookup"><span data-stu-id="1092e-104">Retrieves the system AppPatch directory.</span></span>

## <a name="syntax"></a><span data-ttu-id="1092e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1092e-105">Syntax</span></span>


```C++
void WINAPI SdbGetAppPatchDir(
  _In_opt_ HSDB   hSDB,
  _Out_    LPTSTR szAppPatchPath,
  _In_     DWORD  cchSize
);
```



## <a name="parameters"></a><span data-ttu-id="1092e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1092e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1092e-107">*хсдб* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="1092e-107">*hSDB* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1092e-108">Маркер базы данных оболочек совместимости, возвращаемый функцией [**сдбинитдатабасе**](sdbinitdatabase.md) .</span><span class="sxs-lookup"><span data-stu-id="1092e-108">A handle to the shim database returned by the [**SdbInitDatabase**](sdbinitdatabase.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="1092e-109">*сзапппатчпас* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="1092e-109">*szAppPatchPath* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1092e-110">Результирующий путь.</span><span class="sxs-lookup"><span data-stu-id="1092e-110">The resulting path.</span></span>

</dd> <dt>

<span data-ttu-id="1092e-111">*кчсизе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1092e-111">*cchSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1092e-112">Размер буфера *сзапппатчпас* в символах.</span><span class="sxs-lookup"><span data-stu-id="1092e-112">The size of the *szAppPatchPath* buffer, in characters.</span></span> <span data-ttu-id="1092e-113">Если функция завершается ошибкой, для этого параметра задается пустая строка ("").</span><span class="sxs-lookup"><span data-stu-id="1092e-113">If the function fails, this parameter is set to the empty string ("").</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1092e-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1092e-114">Return value</span></span>

<span data-ttu-id="1092e-115">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="1092e-115">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="1092e-116">Требования</span><span class="sxs-lookup"><span data-stu-id="1092e-116">Requirements</span></span>



| <span data-ttu-id="1092e-117">Требование</span><span class="sxs-lookup"><span data-stu-id="1092e-117">Requirement</span></span> | <span data-ttu-id="1092e-118">Значение</span><span class="sxs-lookup"><span data-stu-id="1092e-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1092e-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1092e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="1092e-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1092e-120">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="1092e-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1092e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="1092e-122">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1092e-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="1092e-123">DLL</span><span class="sxs-lookup"><span data-stu-id="1092e-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1092e-124"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1092e-124"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1092e-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1092e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1092e-126">**сдбинитдатабасе**</span><span class="sxs-lookup"><span data-stu-id="1092e-126">**SdbInitDatabase**</span></span>](sdbinitdatabase.md)
</dt> </dl>

 

 




