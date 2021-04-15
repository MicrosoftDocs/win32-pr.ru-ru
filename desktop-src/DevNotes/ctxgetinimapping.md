---
description: Определяет, находится ли сервер терминалов в режиме установки (только на сервере терминалов Windows 4,0).
ms.assetid: f6cb7971-d4f5-49ca-938a-9c280028764a
title: Функция Ктксжетинимаппинг
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CtxGetIniMapping
api_type:
- DllExport
api_location:
- Kernel32.dll
ms.openlocfilehash: 17093303cf0ea74e7efc6a3070c48660083bc491
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648991"
---
# <a name="ctxgetinimapping-function"></a><span data-ttu-id="8fe9e-103">Функция Ктксжетинимаппинг</span><span class="sxs-lookup"><span data-stu-id="8fe9e-103">CtxGetIniMapping function</span></span>

<span data-ttu-id="8fe9e-104">\[Эта функция не поддерживается и не должна использоваться.</span><span class="sxs-lookup"><span data-stu-id="8fe9e-104">\[This function is not supported and should not be used.</span></span> <span data-ttu-id="8fe9e-105">Он может измениться или исчезнуть полностью без предварительного уведомления.</span><span class="sxs-lookup"><span data-stu-id="8fe9e-105">It may change or disappear completely without advance notice.</span></span> <span data-ttu-id="8fe9e-106">Вместо этого используйте **верифиверсионинфо**.\]</span><span class="sxs-lookup"><span data-stu-id="8fe9e-106">Instead, use **VerifyVersionInfo**.\]</span></span>

<span data-ttu-id="8fe9e-107">Определяет, находится ли сервер терминалов в режиме установки (только на сервере терминалов Windows 4,0).</span><span class="sxs-lookup"><span data-stu-id="8fe9e-107">Determines whether the Terminal Server is in INSTALL mode (only on Windows Terminal Server 4.0).</span></span>

## <a name="syntax"></a><span data-ttu-id="8fe9e-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8fe9e-108">Syntax</span></span>


```C++
BOOLEAN CtxGetIniMapping(void);
```



## <a name="parameters"></a><span data-ttu-id="8fe9e-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="8fe9e-109">Parameters</span></span>

<span data-ttu-id="8fe9e-110">У этой функции нет параметров.</span><span class="sxs-lookup"><span data-stu-id="8fe9e-110">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8fe9e-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8fe9e-111">Return value</span></span>

<span data-ttu-id="8fe9e-112">Эта функция возвращает **значение false** , если сервер терминалов находится в режиме установки, и **значение true** , если он находится в режиме выполнения.</span><span class="sxs-lookup"><span data-stu-id="8fe9e-112">This function returns **FALSE** if the Terminal Server is in INSTALL mode, **TRUE** if it is in EXECUTE mode.</span></span>

## <a name="requirements"></a><span data-ttu-id="8fe9e-113">Требования</span><span class="sxs-lookup"><span data-stu-id="8fe9e-113">Requirements</span></span>



| <span data-ttu-id="8fe9e-114">Требование</span><span class="sxs-lookup"><span data-stu-id="8fe9e-114">Requirement</span></span> | <span data-ttu-id="8fe9e-115">Значение</span><span class="sxs-lookup"><span data-stu-id="8fe9e-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8fe9e-116">DLL</span><span class="sxs-lookup"><span data-stu-id="8fe9e-116">DLL</span></span><br/> | <dl> <span data-ttu-id="8fe9e-117"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8fe9e-117"><dt>Kernel32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8fe9e-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8fe9e-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fe9e-119">**верифиверсионинфо**</span><span class="sxs-lookup"><span data-stu-id="8fe9e-119">**VerifyVersionInfo**</span></span>](/windows/win32/api/winbase/nf-winbase-verifyversioninfoa)
</dt> </dl>

 

 
