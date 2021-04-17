---
description: Метод Опенлог объекта Merge открывает файл журнала, который получает сведения о ходе выполнения и сообщениях об ошибках. Если файл журнала уже существует, установщик добавляет новые сообщения. Если файл журнала не существует, установщик создает файл журнала.
ms.assetid: 97d01ea3-43b6-4529-9706-97b3b0132d9c
title: Метод Merge. Опенлог (Мержемод. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.OpenLog
- IMsmMerge.OpenLog
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 46dc029c88b44540817e93e1e559829d88b9f62b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652295"
---
# <a name="mergeopenlog-method"></a><span data-ttu-id="00221-105">Метод Merge. Опенлог</span><span class="sxs-lookup"><span data-stu-id="00221-105">Merge.OpenLog method</span></span>

<span data-ttu-id="00221-106">Метод **опенлог** объекта [**Merge**](merge-object.md) открывает файл журнала, который получает сведения о ходе выполнения и сообщениях об ошибках.</span><span class="sxs-lookup"><span data-stu-id="00221-106">The **OpenLog** method of the [**Merge**](merge-object.md) object opens a log file that receives progress and error messages.</span></span> <span data-ttu-id="00221-107">Если файл журнала уже существует, установщик добавляет новые сообщения.</span><span class="sxs-lookup"><span data-stu-id="00221-107">If the log file already exists, the installer appends new messages.</span></span> <span data-ttu-id="00221-108">Если файл журнала не существует, установщик создает файл журнала.</span><span class="sxs-lookup"><span data-stu-id="00221-108">If the log file does not exist, the installer creates a log file.</span></span>

## <a name="syntax"></a><span data-ttu-id="00221-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="00221-109">Syntax</span></span>


```JScript
Merge.OpenLog(
  Filename
)
```



## <a name="parameters"></a><span data-ttu-id="00221-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="00221-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00221-111">*Имя файла*</span><span class="sxs-lookup"><span data-stu-id="00221-111">*Filename*</span></span> 
</dt> <dd>

<span data-ttu-id="00221-112">Полное имя файла, указывающее на файл, который нужно открыть или создать.</span><span class="sxs-lookup"><span data-stu-id="00221-112">Fully qualified file name pointing to a file to open or create.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00221-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="00221-113">Return value</span></span>

<span data-ttu-id="00221-114">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="00221-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="00221-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="00221-115">Remarks</span></span>

<span data-ttu-id="00221-116">Клиенты могут отправить свои сообщения в этот файл журнала с помощью метода [**log**](merge-log.md) .</span><span class="sxs-lookup"><span data-stu-id="00221-116">Clients may send their own messages to this log file through the [**Log**](merge-log.md) method.</span></span>

### <a name="c"></a><span data-ttu-id="00221-117">C++</span><span class="sxs-lookup"><span data-stu-id="00221-117">C++</span></span>

<span data-ttu-id="00221-118">См. раздел Функция [**опенлог**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-openlog) .</span><span class="sxs-lookup"><span data-stu-id="00221-118">See [**OpenLog**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-openlog) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="00221-119">Требования</span><span class="sxs-lookup"><span data-stu-id="00221-119">Requirements</span></span>



| <span data-ttu-id="00221-120">Требование</span><span class="sxs-lookup"><span data-stu-id="00221-120">Requirement</span></span> | <span data-ttu-id="00221-121">Значение</span><span class="sxs-lookup"><span data-stu-id="00221-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="00221-122">Версия</span><span class="sxs-lookup"><span data-stu-id="00221-122">Version</span></span><br/> | <span data-ttu-id="00221-123">Mergemod.dll 1,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="00221-123">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="00221-124">Header</span><span class="sxs-lookup"><span data-stu-id="00221-124">Header</span></span><br/>  | <dl> <span data-ttu-id="00221-125"><dt>Мержемод. h</dt></span><span class="sxs-lookup"><span data-stu-id="00221-125"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="00221-126">DLL</span><span class="sxs-lookup"><span data-stu-id="00221-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="00221-127"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="00221-127"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 
