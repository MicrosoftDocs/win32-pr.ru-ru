---
description: Включает или отключает чтение и запись секторов диска.
ms.assetid: 885e4db1-a131-4727-80ab-3be8c591b766
title: Функция Фвинаблеравакцессв
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FveEnableRawAccessW
api_type:
- DllExport
api_location:
- Fveapi.dll
ms.openlocfilehash: 5b4a367c3566c1475f856783d800ec43e21071e2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895670"
---
# <a name="fveenablerawaccessw-function"></a><span data-ttu-id="ba86a-103">Функция Фвинаблеравакцессв</span><span class="sxs-lookup"><span data-stu-id="ba86a-103">FveEnableRawAccessW function</span></span>

<span data-ttu-id="ba86a-104">Включает или отключает чтение и запись секторов диска.</span><span class="sxs-lookup"><span data-stu-id="ba86a-104">Enables or disables reading and writing of disk sectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba86a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ba86a-105">Syntax</span></span>


```C++
HRESULT FveEnableRawAccessW(
  _In_ PCWSTR VolumeName,
  _In_ BOOL   Enabled
);
```



## <a name="parameters"></a><span data-ttu-id="ba86a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ba86a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba86a-107">Переданное  \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ba86a-107">*VolumeName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba86a-108">Уникальный идентификатор тома диска.</span><span class="sxs-lookup"><span data-stu-id="ba86a-108">A unique identifier for the disk volume.</span></span>

</dd> <dt>

<span data-ttu-id="ba86a-109">*Включено* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ba86a-109">*Enabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba86a-110">Если **значение — true**, разрешает доступ к необработанному тому.</span><span class="sxs-lookup"><span data-stu-id="ba86a-110">If **TRUE**, allows access to the raw volume.</span></span> <span data-ttu-id="ba86a-111">Если **значение равно false**, доступ к необработанному тому запрещен.</span><span class="sxs-lookup"><span data-stu-id="ba86a-111">If **FALSE**, no access is allowed to the raw volume.</span></span> <span data-ttu-id="ba86a-112">Если необработанный доступ уже включен, но это значение равно **false**, том повторно подключен и повторно проверяется.</span><span class="sxs-lookup"><span data-stu-id="ba86a-112">If raw access has already been enabled but this value is **FALSE**, the volume is remounted and revalidated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba86a-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ba86a-113">Return value</span></span>

<span data-ttu-id="ba86a-114">Эта функция возвращает один из следующих кодов или другой код ошибки в случае сбоя.</span><span class="sxs-lookup"><span data-stu-id="ba86a-114">This function returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="ba86a-115">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="ba86a-115">Return code/value</span></span>                                                                                                                                                           | <span data-ttu-id="ba86a-116">Описание</span><span class="sxs-lookup"><span data-stu-id="ba86a-116">Description</span></span>                                                                        |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ba86a-117"><dt>**С \_ ОК**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="ba86a-117"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                           | <span data-ttu-id="ba86a-118">Функция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="ba86a-118">The function was successful.</span></span><br/>                                            |
| <dl> <span data-ttu-id="ba86a-119"><dt>**С \_ FALSE**</dt> <dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="ba86a-119"><dt>**S\_FALSE**</dt> <dt>1 (0x1)</dt></span></span> </dl>                        | <span data-ttu-id="ba86a-120">Параметр Enabled имеет **значение false** , а том не находится в режиме доступа RAW.</span><span class="sxs-lookup"><span data-stu-id="ba86a-120">Enabled is **FALSE** and the volume was not already in raw access mode.</span></span><br/> |
| <dl> <span data-ttu-id="ba86a-121"><dt>**Д \_ ACCESSDENIED**</dt> <dt>2147942405 (0x80070005)</dt></span><span class="sxs-lookup"><span data-stu-id="ba86a-121"><dt>**E\_ACCESSDENIED**</dt> <dt>2147942405 (0x80070005)</dt></span></span> </dl> | <span data-ttu-id="ba86a-122">Том не может быть заблокирован.</span><span class="sxs-lookup"><span data-stu-id="ba86a-122">The volume cannot be locked.</span></span><br/>                                            |



 

## <a name="requirements"></a><span data-ttu-id="ba86a-123">Требования</span><span class="sxs-lookup"><span data-stu-id="ba86a-123">Requirements</span></span>



| <span data-ttu-id="ba86a-124">Требование</span><span class="sxs-lookup"><span data-stu-id="ba86a-124">Requirement</span></span> | <span data-ttu-id="ba86a-125">Значение</span><span class="sxs-lookup"><span data-stu-id="ba86a-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ba86a-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ba86a-126">Minimum supported client</span></span><br/> | <span data-ttu-id="ba86a-127">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ba86a-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ba86a-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ba86a-128">Minimum supported server</span></span><br/> | <span data-ttu-id="ba86a-129">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ba86a-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ba86a-130">DLL</span><span class="sxs-lookup"><span data-stu-id="ba86a-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ba86a-131"><dt>Fveapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ba86a-131"><dt>Fveapi.dll</dt></span></span> </dl> |



 

 




