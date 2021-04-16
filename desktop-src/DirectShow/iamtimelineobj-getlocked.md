---
description: Метод NOLOCK Извлекает состояние редактирования объекта (заблокировано или разблокировано).
ms.assetid: ecd258db-36bf-41b6-9bdf-537efcf0a46a
title: 'Метод Иамтимелинеобж:: NOLOCK (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetLocked
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 472b7dedbdbd879d4fa49fe874fb9178d0ccdee4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679666"
---
# <a name="iamtimelineobjgetlocked-method"></a><span data-ttu-id="b6e97-103">Метод Иамтимелинеобж:: NOLOCK</span><span class="sxs-lookup"><span data-stu-id="b6e97-103">IAMTimelineObj::GetLocked method</span></span>

> [!Note]  
> <span data-ttu-id="b6e97-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="b6e97-104">\[Deprecated.</span></span> <span data-ttu-id="b6e97-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b6e97-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="b6e97-106">`GetLocked`Метод получает состояние редактирования объекта (заблокировано или разблокировано).</span><span class="sxs-lookup"><span data-stu-id="b6e97-106">The `GetLocked` method retrieves the object's editing state (locked or unlocked).</span></span> <span data-ttu-id="b6e97-107">Заблокированное состояние указывает, что объект не должен редактироваться; незаблокированное состояние указывает, что объект можно изменять.</span><span class="sxs-lookup"><span data-stu-id="b6e97-107">A locked state indicates that the object should not be edited; an unlocked state indicates that the object can be edited.</span></span> <span data-ttu-id="b6e97-108">Временная шкала не обеспечивает принудительную блокировку.</span><span class="sxs-lookup"><span data-stu-id="b6e97-108">The timeline does not enforce the lock.</span></span> <span data-ttu-id="b6e97-109">Параметр блокировки существует только для удобства приложения.</span><span class="sxs-lookup"><span data-stu-id="b6e97-109">The locked setting exists only for the convenience of the application.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6e97-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b6e97-110">Syntax</span></span>


```C++
 GetLocked(
   BOOL *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="b6e97-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="b6e97-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6e97-112">*pVal*</span><span class="sxs-lookup"><span data-stu-id="b6e97-112">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="b6e97-113">Получает состояние редактирования объекта.</span><span class="sxs-lookup"><span data-stu-id="b6e97-113">Receives the object's editing state.</span></span> <span data-ttu-id="b6e97-114">Если значение равно **true**, объект заблокирован и не должен редактироваться.</span><span class="sxs-lookup"><span data-stu-id="b6e97-114">If the value is **TRUE**, the object is locked and should not be edited.</span></span> <span data-ttu-id="b6e97-115">Если **значение равно false**, объект разблокируется и может быть изменен.</span><span class="sxs-lookup"><span data-stu-id="b6e97-115">If **FALSE**, the object is unlocked and can be edited.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b6e97-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b6e97-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b6e97-117">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="b6e97-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="b6e97-118">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="b6e97-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="b6e97-119">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="b6e97-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b6e97-120">Требования</span><span class="sxs-lookup"><span data-stu-id="b6e97-120">Requirements</span></span>



| <span data-ttu-id="b6e97-121">Требование</span><span class="sxs-lookup"><span data-stu-id="b6e97-121">Requirement</span></span> | <span data-ttu-id="b6e97-122">Значение</span><span class="sxs-lookup"><span data-stu-id="b6e97-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b6e97-123">Header</span><span class="sxs-lookup"><span data-stu-id="b6e97-123">Header</span></span><br/>  | <dl> <span data-ttu-id="b6e97-124"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6e97-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="b6e97-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b6e97-125">Library</span></span><br/> | <dl> <span data-ttu-id="b6e97-126"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b6e97-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6e97-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b6e97-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6e97-128">**Интерфейс Иамтимелинеобж**</span><span class="sxs-lookup"><span data-stu-id="b6e97-128">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="b6e97-129">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="b6e97-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




