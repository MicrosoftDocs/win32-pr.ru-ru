---
title: Метод Ивмдрмлиценсебаккупресторестатус-Status (Вмдрмсдк. h)
description: Метод WebMethod получает подробные сведения о состоянии операции резервного копирования или восстановления лицензий.
ms.assetid: 1a695baf-0971-4dbf-90fa-1b10178a3348
keywords:
- Метод WebMethod формат Windows Media Format
- Метод WebMethod формат Windows Media Format, интерфейс Ивмдрмлиценсебаккупресторестатус
- Интерфейс Ивмдрмлиценсебаккупресторестатус интерфейса Windows Media Format, методического состояния
topic_type:
- apiref
api_name:
- IWMDRMLicenseBackupRestoreStatus.GetStatus
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3373e71bcae9dc1054e97e8b758ac72389b9a712
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708522"
---
# <a name="iwmdrmlicensebackuprestorestatusgetstatus-method"></a><span data-ttu-id="8dc39-106">Метод Ивмдрмлиценсебаккупресторестатус:: with Status</span><span class="sxs-lookup"><span data-stu-id="8dc39-106">IWMDRMLicenseBackupRestoreStatus::GetStatus method</span></span>

<span data-ttu-id="8dc39-107">Метод WebMethod получает подробные сведения **о состоянии операции** резервного копирования или восстановления лицензий.</span><span class="sxs-lookup"><span data-stu-id="8dc39-107">The **GetStatus** method retrieves detailed status information about a license backup or restore operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="8dc39-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8dc39-108">Syntax</span></span>


```C++
HRESULT GetStatus(
  [out] WM_BACKUP_RESTORE_STATUS *pStatus
);
```



## <a name="parameters"></a><span data-ttu-id="8dc39-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="8dc39-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8dc39-110">*пстатус* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="8dc39-110">*pStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8dc39-111">Указатель на структуру [**\_ \_ \_ состояния восстановления резервной копии WM**](wm-backup-restore-status.md) , которая получает сведения о состоянии.</span><span class="sxs-lookup"><span data-stu-id="8dc39-111">Pointer to a [**WM\_BACKUP\_RESTORE\_STATUS**](wm-backup-restore-status.md) structure that receives the status information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8dc39-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8dc39-112">Return value</span></span>

<span data-ttu-id="8dc39-113">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="8dc39-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="8dc39-114">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="8dc39-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="8dc39-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="8dc39-115">Return code</span></span>                                                                          | <span data-ttu-id="8dc39-116">Описание</span><span class="sxs-lookup"><span data-stu-id="8dc39-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="8dc39-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="8dc39-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="8dc39-118">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="8dc39-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8dc39-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8dc39-119">Remarks</span></span>

<span data-ttu-id="8dc39-120">Нет.</span><span class="sxs-lookup"><span data-stu-id="8dc39-120">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="8dc39-121">Требования</span><span class="sxs-lookup"><span data-stu-id="8dc39-121">Requirements</span></span>



| <span data-ttu-id="8dc39-122">Требование</span><span class="sxs-lookup"><span data-stu-id="8dc39-122">Requirement</span></span> | <span data-ttu-id="8dc39-123">Значение</span><span class="sxs-lookup"><span data-stu-id="8dc39-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8dc39-124">Header</span><span class="sxs-lookup"><span data-stu-id="8dc39-124">Header</span></span><br/>  | <dl> <span data-ttu-id="8dc39-125"><dt>Вмдрмсдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="8dc39-125"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="8dc39-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8dc39-126">Library</span></span><br/> | <dl> <span data-ttu-id="8dc39-127"><dt>Вмдрмсдк. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8dc39-127"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8dc39-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8dc39-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8dc39-129">**Интерфейс Ивмдрмлиценсебаккупресторестатус**</span><span class="sxs-lookup"><span data-stu-id="8dc39-129">**IWMDRMLicenseBackupRestoreStatus Interface**</span></span>](iwmdrmlicensebackuprestorestatus.md)
</dt> </dl>

 

 





