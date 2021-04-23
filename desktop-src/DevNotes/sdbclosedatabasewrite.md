---
description: Закрывает указанную базу данных.
ms.assetid: 69546f03-9912-401a-9c1a-b7fdbe16dbf8
title: Функция Сдбклоседатабасеврите
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbCloseDatabaseWrite
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 24df6f9ce2c4f0fae4dd1c1ef244e006ea00c047
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895753"
---
# <a name="sdbclosedatabasewrite-function"></a><span data-ttu-id="0a717-103">Функция Сдбклоседатабасеврите</span><span class="sxs-lookup"><span data-stu-id="0a717-103">SdbCloseDatabaseWrite function</span></span>

<span data-ttu-id="0a717-104">Закрывает указанную базу данных.</span><span class="sxs-lookup"><span data-stu-id="0a717-104">Closes the specified database.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a717-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0a717-105">Syntax</span></span>


```C++
void WINAPI SdbCloseDatabaseWrite(
  _Inout_ PDB pdb
);
```



## <a name="parameters"></a><span data-ttu-id="0a717-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0a717-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a717-107">*pdb* \[ -файл в, out\]</span><span class="sxs-lookup"><span data-stu-id="0a717-107">*pdb* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0a717-108">Маркер базы данных оболочек совместимости.</span><span class="sxs-lookup"><span data-stu-id="0a717-108">A handle to the shim database.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a717-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0a717-109">Return value</span></span>

<span data-ttu-id="0a717-110">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="0a717-110">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0a717-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0a717-111">Remarks</span></span>

<span data-ttu-id="0a717-112">Эта функция вызывает [**сдбклоседатабасе**](sdbclosedatabase.md); Поэтому эти две функции эквивалентны.</span><span class="sxs-lookup"><span data-stu-id="0a717-112">This function calls [**SdbCloseDatabase**](sdbclosedatabase.md); therefore, these two functions are equivalent.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a717-113">Требования</span><span class="sxs-lookup"><span data-stu-id="0a717-113">Requirements</span></span>



| <span data-ttu-id="0a717-114">Требование</span><span class="sxs-lookup"><span data-stu-id="0a717-114">Requirement</span></span> | <span data-ttu-id="0a717-115">Значение</span><span class="sxs-lookup"><span data-stu-id="0a717-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0a717-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0a717-116">Minimum supported client</span></span><br/> | <span data-ttu-id="0a717-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0a717-117">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="0a717-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0a717-118">Minimum supported server</span></span><br/> | <span data-ttu-id="0a717-119">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0a717-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="0a717-120">DLL</span><span class="sxs-lookup"><span data-stu-id="0a717-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0a717-121"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0a717-121"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a717-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0a717-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a717-123">**сдббегинврителисттаг**</span><span class="sxs-lookup"><span data-stu-id="0a717-123">**SdbBeginWriteListTag**</span></span>](sdbbeginwritelisttag.md)
</dt> <dt>

[<span data-ttu-id="0a717-124">**сдбклоседатабасе**</span><span class="sxs-lookup"><span data-stu-id="0a717-124">**SdbCloseDatabase**</span></span>](sdbclosedatabase.md)
</dt> <dt>

[<span data-ttu-id="0a717-125">**сдбендврителисттаг**</span><span class="sxs-lookup"><span data-stu-id="0a717-125">**SdbEndWriteListTag**</span></span>](sdbendwritelisttag.md)
</dt> </dl>

 

 




