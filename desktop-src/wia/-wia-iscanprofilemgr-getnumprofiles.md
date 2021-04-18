---
description: Возвращает число профилей сканирования, созданных для пользователя в системе, в которой выполняется приложение.
ms.assetid: 0667a885-d61f-4c44-b988-a42242c2678e
title: 'Метод Исканпрофилемгр:: Жетнумпрофилес (Сканпрофилемгр. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.GetNumProfiles
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: a8c3167bd428054054a32d7823ce57e562501533
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105702225"
---
# <a name="iscanprofilemgrgetnumprofiles-method"></a><span data-ttu-id="aaa94-103">Метод Исканпрофилемгр:: Жетнумпрофилес</span><span class="sxs-lookup"><span data-stu-id="aaa94-103">IScanProfileMgr::GetNumProfiles method</span></span>

<span data-ttu-id="aaa94-104">Возвращает число профилей сканирования, созданных для пользователя в системе, в которой выполняется приложение.</span><span class="sxs-lookup"><span data-stu-id="aaa94-104">Gets the number of scan profiles created for the user in the system that your application is running under.</span></span>

## <a name="syntax"></a><span data-ttu-id="aaa94-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="aaa94-105">Syntax</span></span>


```C++
HRESULT GetNumProfiles(
  [out] ULONG *pulNumProfiles
);
```



## <a name="parameters"></a><span data-ttu-id="aaa94-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="aaa94-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aaa94-107">*пулнумпрофилес* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="aaa94-107">*pulNumProfiles* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="aaa94-108">Тип: \**ulong \** _</span><span class="sxs-lookup"><span data-stu-id="aaa94-108">Type: \**ULONG\** _</span></span>

<span data-ttu-id="aaa94-109">Указатель на число профилей, созданных для пользователя.</span><span class="sxs-lookup"><span data-stu-id="aaa94-109">A pointer to the number of profiles created for the user.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aaa94-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="aaa94-110">Return value</span></span>

<span data-ttu-id="aaa94-111">Тип: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="aaa94-111">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="aaa94-112">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="aaa94-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="aaa94-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="aaa94-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="aaa94-114">Требования</span><span class="sxs-lookup"><span data-stu-id="aaa94-114">Requirements</span></span>



| <span data-ttu-id="aaa94-115">Требование</span><span class="sxs-lookup"><span data-stu-id="aaa94-115">Requirement</span></span> | <span data-ttu-id="aaa94-116">Значение</span><span class="sxs-lookup"><span data-stu-id="aaa94-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="aaa94-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="aaa94-117">Minimum supported client</span></span><br/> | <span data-ttu-id="aaa94-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="aaa94-118">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="aaa94-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="aaa94-119">Minimum supported server</span></span><br/> | <span data-ttu-id="aaa94-120">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="aaa94-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="aaa94-121">Header</span><span class="sxs-lookup"><span data-stu-id="aaa94-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="aaa94-122"><dt>Сканпрофилемгр. h</dt></span><span class="sxs-lookup"><span data-stu-id="aaa94-122"><dt>Scanprofilemgr.h</dt></span></span> </dl> |
| <span data-ttu-id="aaa94-123">IDL</span><span class="sxs-lookup"><span data-stu-id="aaa94-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="aaa94-124"><dt>Сканпрофилес. idl</dt></span><span class="sxs-lookup"><span data-stu-id="aaa94-124"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aaa94-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="aaa94-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aaa94-126">**исканпрофилемгр**</span><span class="sxs-lookup"><span data-stu-id="aaa94-126">**IScanProfileMgr**</span></span>](-wia-iscanprofilemgr.md)
</dt> <dt>

[<span data-ttu-id="aaa94-127">Схема профиля сканирования</span><span class="sxs-lookup"><span data-stu-id="aaa94-127">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




