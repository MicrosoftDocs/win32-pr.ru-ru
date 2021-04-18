---
title: delete cache
description: Очищает весь кэш URL-адресов или удаляет записи в соответствии с указанным URL-адресом.
ms.assetid: 499ce0f9-01db-4648-89f7-1ecafd25a805
keywords:
- удалить HTTP-кэш кэша
topic_type:
- apiref
api_name:
- delete cache
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f963d12812140d11923460235ef780a621ba3db5
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2019
ms.locfileid: "105681572"
---
# <a name="delete-cache"></a><span data-ttu-id="7df0f-104">delete cache</span><span class="sxs-lookup"><span data-stu-id="7df0f-104">delete cache</span></span>

<span data-ttu-id="7df0f-105">Очищает весь кэш URL-адресов или удаляет записи в соответствии с указанным URL-адресом.</span><span class="sxs-lookup"><span data-stu-id="7df0f-105">Flushes the entire URL cache or deletes entries according to the specified URL.</span></span>

``` syntax
delete cache [url=]string [[recursive=]{yes|no}]
 
```

## <a name="parameters"></a><span data-ttu-id="7df0f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7df0f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7df0f-107"><span id="_url__string"></span><span id="_URL__STRING"></span>\**\[URL = \] \* \* \* строка*</span><span class="sxs-lookup"><span data-stu-id="7df0f-107"><span id="_url__string"></span><span id="_URL__STRING"></span>\**\[url=\]\*\*\*string*</span></span>
</dt> <dd>

<span data-ttu-id="7df0f-108">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="7df0f-108">Required.</span></span> <span data-ttu-id="7df0f-109">Указывает полный URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="7df0f-109">Specifies the fully qualified URL.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="7df0f-110"><span id="_recursive___yes_no_"></span><span id="_RECURSIVE___YES_NO_"></span>**\[recursive = \] {Да \| нет}**</span><span class="sxs-lookup"><span data-stu-id="7df0f-110"><span id="_recursive___yes_no_"></span><span id="_RECURSIVE___YES_NO_"></span>**\[recursive=\]{yes\|no}**</span></span>
</dt> <dd>

<span data-ttu-id="7df0f-111">Если да, удаляет все записи с указанным URL-адресом.</span><span class="sxs-lookup"><span data-stu-id="7df0f-111">If yes, removes all entries under the specified URL.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="7df0f-112">Примеры</span><span class="sxs-lookup"><span data-stu-id="7df0f-112">Examples</span></span>

<span data-ttu-id="7df0f-113">**удалить URL-адрес кэша = https://www.contoso.com:80/myresource/ recursive = да**</span><span class="sxs-lookup"><span data-stu-id="7df0f-113">**delete cache url=https://www.contoso.com:80/myresource/ recursive=yes**</span></span>

 

 




