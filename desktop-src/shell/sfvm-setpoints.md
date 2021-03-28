---
description: Задает точки выбранных в данный момент объектов для объекта данных в командах копирования и вырезания. Используется \_ сообщением шшеллфолдервиев.
title: Сообщение SFVM_SETPOINTS (Шлобж. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: d2c3e06a-19e4-4b78-9b7c-1a256582786e
api_name:
- SFVM_SETPOINTS
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 1df501f162fb19335fcf1672299a74135672db22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272847"
---
# <a name="sfvm_setpoints-message"></a><span data-ttu-id="2b929-104">\_Сообщение сфвм сетпоинтс</span><span class="sxs-lookup"><span data-stu-id="2b929-104">SFVM\_SETPOINTS message</span></span>

<span data-ttu-id="2b929-105">Задает точки выбранных в данный момент объектов для объекта данных в командах **копирования** и **вырезания** .</span><span class="sxs-lookup"><span data-stu-id="2b929-105">Sets the points of the currently selected objects to the data object on **Copy** and **Cut** commands.</span></span> <span data-ttu-id="2b929-106">Используется [**\_ сообщением шшеллфолдервиев**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).</span><span class="sxs-lookup"><span data-stu-id="2b929-106">Used by [**SHShellFolderView\_Message**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).</span></span>


```C++
SFVM_SETPOINTS 

    lParam = (LPARAM) pdtobj;

            
```



## <a name="parameters"></a><span data-ttu-id="2b929-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="2b929-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b929-108">*пдтобж* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2b929-108">*pdtobj* \[in\]</span></span>
</dt> <dd><span data-ttu-id="2b929-109">Указатель на <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">**IDataObject**</a> команд **Copy** и **Cut** .</span><span class="sxs-lookup"><span data-stu-id="2b929-109">A pointer to an <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">**IDataObject**</a> of the **Copy** and **Cut** commands.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b929-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2b929-110">Return value</span></span>

<span data-ttu-id="2b929-111">Всегда возвращает значение 0.</span><span class="sxs-lookup"><span data-stu-id="2b929-111">Always returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b929-112">Remarks</span><span class="sxs-lookup"><span data-stu-id="2b929-112">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="2b929-113">Требования</span><span class="sxs-lookup"><span data-stu-id="2b929-113">Requirements</span></span>



| <span data-ttu-id="2b929-114">Требование</span><span class="sxs-lookup"><span data-stu-id="2b929-114">Requirement</span></span> | <span data-ttu-id="2b929-115">Значение</span><span class="sxs-lookup"><span data-stu-id="2b929-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="2b929-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2b929-116">Minimum supported client</span></span><br/> | <span data-ttu-id="2b929-117">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2b929-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="2b929-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2b929-118">Minimum supported server</span></span><br/> | <span data-ttu-id="2b929-119">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2b929-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="2b929-120">Заголовок</span><span class="sxs-lookup"><span data-stu-id="2b929-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="2b929-121"><dt>Шлобж. h</dt></span><span class="sxs-lookup"><span data-stu-id="2b929-121"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
