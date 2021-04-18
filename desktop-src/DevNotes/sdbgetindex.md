---
description: Извлекает индекс указанного тега и типа ключа из указанной базы данных.
ms.assetid: 5fa44252-ba26-43ed-9de0-5917e4ec797c
title: Функция Сдбжетиндекс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetIndex
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: c7bcc211e4277a2ffee6a68258d7616cb7aa2a0c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496176"
---
# <a name="sdbgetindex-function"></a><span data-ttu-id="3d273-103">Функция Сдбжетиндекс</span><span class="sxs-lookup"><span data-stu-id="3d273-103">SdbGetIndex function</span></span>

<span data-ttu-id="3d273-104">Извлекает индекс указанного тега и типа ключа из указанной базы данных.</span><span class="sxs-lookup"><span data-stu-id="3d273-104">Retrieves the index for the specified tag and key type from the specified database.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d273-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3d273-105">Syntax</span></span>


```C++
TAGID WINAPI SdbGetIndex(
  _In_      PDB     pdb,
  _In_      TAG     tWhich,
  _In_      TAG     tKey,
  _Out_opt_ LPDWORD lpdwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="3d273-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3d273-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d273-107">*pdb* \[ -файл окне\]</span><span class="sxs-lookup"><span data-stu-id="3d273-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d273-108">Маркер базы данных оболочек совместимости.</span><span class="sxs-lookup"><span data-stu-id="3d273-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="3d273-109">*твхич* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3d273-109">*tWhich* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d273-110">ТЕГ.</span><span class="sxs-lookup"><span data-stu-id="3d273-110">The TAG.</span></span>

</dd> <dt>

<span data-ttu-id="3d273-111">*tKey* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3d273-111">*tKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d273-112">Тип ключа.</span><span class="sxs-lookup"><span data-stu-id="3d273-112">The key type.</span></span>

</dd> <dt>

<span data-ttu-id="3d273-113">*лпдвфлагс* \[ out, необязательно\]</span><span class="sxs-lookup"><span data-stu-id="3d273-113">*lpdwFlags* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3d273-114">Этот параметр может быть равен 0 **или \_ шимдб \_ уникальному \_ ключу индекса** (0x00000001).</span><span class="sxs-lookup"><span data-stu-id="3d273-114">This parameter can be 0 or **SHIMDB\_INDEX\_UNIQUE\_KEY** (0x00000001).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d273-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3d273-115">Return value</span></span>

<span data-ttu-id="3d273-116">**TAGID** индекса или **TAGID \_ null**.</span><span class="sxs-lookup"><span data-stu-id="3d273-116">The **TAGID** of the index or **TAGID\_NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="3d273-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3d273-117">Remarks</span></span>

<span data-ttu-id="3d273-118">Полученный индекс можно использовать для операций чтения.</span><span class="sxs-lookup"><span data-stu-id="3d273-118">The resulting index can be used for read operations.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d273-119">Требования</span><span class="sxs-lookup"><span data-stu-id="3d273-119">Requirements</span></span>



| <span data-ttu-id="3d273-120">Требование</span><span class="sxs-lookup"><span data-stu-id="3d273-120">Requirement</span></span> | <span data-ttu-id="3d273-121">Значение</span><span class="sxs-lookup"><span data-stu-id="3d273-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3d273-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3d273-122">Minimum supported client</span></span><br/> | <span data-ttu-id="3d273-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3d273-123">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="3d273-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3d273-124">Minimum supported server</span></span><br/> | <span data-ttu-id="3d273-125">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3d273-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="3d273-126">DLL</span><span class="sxs-lookup"><span data-stu-id="3d273-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3d273-127"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3d273-127"><dt>Apphelp.dll</dt></span></span> </dl> |



 

 




