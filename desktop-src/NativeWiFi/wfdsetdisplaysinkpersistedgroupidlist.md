---
description: Задает список идентификаторов сохраненной группы для всех профилей, сохраняемых приложением.
ms.assetid: EF83F295-CD53-45A4-B209-560B4069CA7C
title: Функция Вфддисплайсинксетперсистедграупидлист (Вфдсинк. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFDSetDisplaySinkPersistedGroupIDList
api_type:
- DllExport
api_location:
- wifidisplay.dll
ms.openlocfilehash: 423360d7127f331fd1aa2de7f7370daebcc2b417
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662699"
---
# <a name="wfddisplaysinksetpersistedgroupidlist-function"></a><span data-ttu-id="60363-103">Функция Вфддисплайсинксетперсистедграупидлист</span><span class="sxs-lookup"><span data-stu-id="60363-103">WFDDisplaySinkSetPersistedGroupIDList function</span></span>

<span data-ttu-id="60363-104">Задает список идентификаторов сохраненной группы для всех профилей, сохраняемых приложением.</span><span class="sxs-lookup"><span data-stu-id="60363-104">Sets the persisted group id list for all the profiles that are persisted by your app.</span></span> <span data-ttu-id="60363-105">Приложение должно вызывать этот метод при каждом добавлении или удалении профиля из своего хранилища.</span><span class="sxs-lookup"><span data-stu-id="60363-105">Your app should call this method every time it adds or deletes a profile from its storage.</span></span>

## <a name="syntax"></a><span data-ttu-id="60363-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="60363-106">Syntax</span></span>


```C++
DWORD WINAPI WFDSetDisplaySinkPersistedGroupIDList(
  _In_ UINT32             cGroupIDList,
  _In_ DOT11_WFD_GROUP_ID *pGroupIDList
);
```



## <a name="parameters"></a><span data-ttu-id="60363-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="60363-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60363-108">*кграупидлист* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="60363-108">*cGroupIDList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60363-109">Число идентификаторов групп, на которые указывает *пграупидлист*.</span><span class="sxs-lookup"><span data-stu-id="60363-109">The count of group ids being pointed to by *pGroupIDList*.</span></span>

</dd> <dt>

<span data-ttu-id="60363-110">*пграупидлист* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="60363-110">*pGroupIDList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60363-111">Указатель на массив идентификаторов групп *кграупидлист* .</span><span class="sxs-lookup"><span data-stu-id="60363-111">Pointer to an array of *cGroupIDList* group ids.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60363-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="60363-112">Return value</span></span>

<span data-ttu-id="60363-113">Если функция завершается успешно, возвращается значение ошибки \_ Success.</span><span class="sxs-lookup"><span data-stu-id="60363-113">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

## <a name="remarks"></a><span data-ttu-id="60363-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="60363-114">Remarks</span></span>

<span data-ttu-id="60363-115">Этот метод всегда должен вызываться со всем списком, а не подмножеством.</span><span class="sxs-lookup"><span data-stu-id="60363-115">This method is always expected to be called with the entire list, and not a subset.</span></span> <span data-ttu-id="60363-116">Этот метод можно вызывать с 0 профилями, если хранилище профиля пусто.</span><span class="sxs-lookup"><span data-stu-id="60363-116">It is OK to call this method with 0 profiles when the profile store is empty.</span></span>

<span data-ttu-id="60363-117">Вызов повторного вызова для идентификатора группы, не входящего в предоставленный список, завершится ошибкой "Failed; неизвестная группа P2P "(состояние 8).</span><span class="sxs-lookup"><span data-stu-id="60363-117">A re-invoke for a group id that is not part of the provided list will fail with "Fail; unknown P2P Group"(status 8).</span></span>

## <a name="requirements"></a><span data-ttu-id="60363-118">Требования</span><span class="sxs-lookup"><span data-stu-id="60363-118">Requirements</span></span>



| <span data-ttu-id="60363-119">Требование</span><span class="sxs-lookup"><span data-stu-id="60363-119">Requirement</span></span> | <span data-ttu-id="60363-120">Значение</span><span class="sxs-lookup"><span data-stu-id="60363-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="60363-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="60363-121">Minimum supported client</span></span><br/> | <span data-ttu-id="60363-122">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="60363-122">Windows 8.1 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="60363-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="60363-123">Minimum supported server</span></span><br/> | <span data-ttu-id="60363-124">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="60363-124">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="60363-125">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="60363-125">End of client support</span></span><br/>    | <span data-ttu-id="60363-126">Windows 10</span><span class="sxs-lookup"><span data-stu-id="60363-126">Windows 10</span></span><br/>                                                                      |
| <span data-ttu-id="60363-127">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="60363-127">End of server support</span></span><br/>    | <span data-ttu-id="60363-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="60363-128">Windows Server 2016</span></span><br/>                                                             |
| <span data-ttu-id="60363-129">Header</span><span class="sxs-lookup"><span data-stu-id="60363-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="60363-130"><dt>Вфдсинк. h</dt></span><span class="sxs-lookup"><span data-stu-id="60363-130"><dt>Wfdsink.h</dt></span></span> </dl>       |
| <span data-ttu-id="60363-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="60363-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="60363-132"><dt>Вифидисплай. lib</dt></span><span class="sxs-lookup"><span data-stu-id="60363-132"><dt>Wifidisplay.lib</dt></span></span> </dl> |
| <span data-ttu-id="60363-133">DLL</span><span class="sxs-lookup"><span data-stu-id="60363-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="60363-134"><dt>Wifidisplay.dll</dt></span><span class="sxs-lookup"><span data-stu-id="60363-134"><dt>Wifidisplay.dll</dt></span></span> </dl> |



 

 




