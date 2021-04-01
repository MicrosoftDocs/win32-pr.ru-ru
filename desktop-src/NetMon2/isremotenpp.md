---
description: Функция Исремотенпп указывает, указывает ли заданный большой двоичный объект удаленный НПП.
ms.assetid: 66ee0a9a-3199-479f-baec-da6ae6b46c65
title: Функция Исремотенпп (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IsRemoteNPP
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: c52346f368c0720601423f258e4dc73c27296311
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812694"
---
# <a name="isremotenpp-function"></a><span data-ttu-id="10659-103">Функция Исремотенпп</span><span class="sxs-lookup"><span data-stu-id="10659-103">IsRemoteNPP function</span></span>

<span data-ttu-id="10659-104">Функция **исремотенпп** указывает, указывает ли заданный большой двоичный объект удаленный НПП.</span><span class="sxs-lookup"><span data-stu-id="10659-104">The **IsRemoteNPP** function indicates whether the given BLOB specifies a remote NPP.</span></span>

## <a name="syntax"></a><span data-ttu-id="10659-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="10659-105">Syntax</span></span>


```C++
BOOL IsRemoteNPP(
  _In_ HBLOB hBlob
);
```



## <a name="parameters"></a><span data-ttu-id="10659-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="10659-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10659-107">*хблоб* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="10659-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="10659-108">Обработчик для большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="10659-108">Handle to a BLOB.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10659-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="10659-109">Return value</span></span>

<span data-ttu-id="10659-110">Если функция выполнена успешно, возвращается значение **true**.</span><span class="sxs-lookup"><span data-stu-id="10659-110">If the function is successful, the return value is **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="10659-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="10659-111">Remarks</span></span>

<span data-ttu-id="10659-112">Используйте эту функцию, чтобы проверить, существует ли удаленная Категория.</span><span class="sxs-lookup"><span data-stu-id="10659-112">Use this function to test whether a remote category exists.</span></span>

<span data-ttu-id="10659-113">Убедитесь, что имена удаленного и локального компьютеров отличаются.</span><span class="sxs-lookup"><span data-stu-id="10659-113">Make certain that the remote and local computer names are different.</span></span>

## <a name="requirements"></a><span data-ttu-id="10659-114">Требования</span><span class="sxs-lookup"><span data-stu-id="10659-114">Requirements</span></span>



| <span data-ttu-id="10659-115">Требование</span><span class="sxs-lookup"><span data-stu-id="10659-115">Requirement</span></span> | <span data-ttu-id="10659-116">Значение</span><span class="sxs-lookup"><span data-stu-id="10659-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="10659-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="10659-117">Minimum supported client</span></span><br/> | <span data-ttu-id="10659-118">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="10659-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="10659-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="10659-119">Minimum supported server</span></span><br/> | <span data-ttu-id="10659-120">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="10659-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="10659-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="10659-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="10659-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="10659-122"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="10659-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="10659-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="10659-124"><dt>Нпптулс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="10659-124"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="10659-125">DLL</span><span class="sxs-lookup"><span data-stu-id="10659-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="10659-126"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="10659-126"><dt>Npptools.dll</dt></span></span> </dl> |



 

 




