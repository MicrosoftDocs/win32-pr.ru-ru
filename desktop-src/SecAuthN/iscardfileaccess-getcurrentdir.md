---
description: Метод Жеткуррентдир возвращает абсолютный путь к текущему выбранному каталогу.
ms.assetid: 12196143-a98a-4772-a803-d0c9b95a66e4
title: 'Метод Искардфилеакцесс:: Жеткуррентдир'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.GetCurrentDir
api_type:
- COM
api_location: ''
ms.openlocfilehash: a779dca10a94250bf4b500585b8b50238b0267dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272771"
---
# <a name="iscardfileaccessgetcurrentdir-method"></a><span data-ttu-id="69013-103">Метод Искардфилеакцесс:: Жеткуррентдир</span><span class="sxs-lookup"><span data-stu-id="69013-103">ISCardFileAccess::GetCurrentDir method</span></span>

<span data-ttu-id="69013-104">\[Метод **жеткуррентдир** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="69013-104">\[The **GetCurrentDir** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="69013-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="69013-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="69013-106">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="69013-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="69013-107">Метод **жеткуррентдир** возвращает абсолютный путь к текущему выбранному каталогу.</span><span class="sxs-lookup"><span data-stu-id="69013-107">The **GetCurrentDir** method returns an absolute path to the currently selected directory.</span></span>

## <a name="syntax"></a><span data-ttu-id="69013-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="69013-108">Syntax</span></span>


```C++
HRESULT GetCurrentDir(
  [out] BSTR *pbstrPathSpec
);
```



## <a name="parameters"></a><span data-ttu-id="69013-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="69013-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69013-110">*пбстрпасспек* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="69013-110">*pbstrPathSpec* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="69013-111">Указатель на BSTR, который будет содержать путь.</span><span class="sxs-lookup"><span data-stu-id="69013-111">Pointer to a BSTR that will contain the path.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69013-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="69013-112">Return value</span></span>

<span data-ttu-id="69013-113">Метод возвращает одно из следующих возможных значений.</span><span class="sxs-lookup"><span data-stu-id="69013-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="69013-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="69013-114">Return code</span></span>                                                                                   | <span data-ttu-id="69013-115">Описание</span><span class="sxs-lookup"><span data-stu-id="69013-115">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="69013-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="69013-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="69013-117">Operation completed successfully (Операция выполнена успешно).</span><span class="sxs-lookup"><span data-stu-id="69013-117">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="69013-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="69013-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="69013-119">Недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="69013-119">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="69013-120"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="69013-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="69013-121">Передан неверный указатель.</span><span class="sxs-lookup"><span data-stu-id="69013-121">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="69013-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="69013-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="69013-123">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="69013-123">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="69013-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="69013-124">Remarks</span></span>

<span data-ttu-id="69013-125">Чтобы изменить текущий каталог, вызовите [**чанжедир**](iscardfileaccess-changedir.md).</span><span class="sxs-lookup"><span data-stu-id="69013-125">To change the current directory, call [**ChangeDir**](iscardfileaccess-changedir.md).</span></span>

<span data-ttu-id="69013-126">Список всех методов, определенных этим интерфейсом, см. в разделе [**искардфилеакцесс**](iscardfileaccess.md).</span><span class="sxs-lookup"><span data-stu-id="69013-126">For a list of all the methods defined by this interface, see [**ISCardFileAccess**](iscardfileaccess.md).</span></span>

<span data-ttu-id="69013-127">Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки [*смарт-карты*](../secgloss/s-gly.md) , если для завершения запроса была вызвана функция смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="69013-127">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="69013-128">Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="69013-128">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="69013-129">Требования</span><span class="sxs-lookup"><span data-stu-id="69013-129">Requirements</span></span>



| <span data-ttu-id="69013-130">Требование</span><span class="sxs-lookup"><span data-stu-id="69013-130">Requirement</span></span> | <span data-ttu-id="69013-131">Значение</span><span class="sxs-lookup"><span data-stu-id="69013-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="69013-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="69013-132">Minimum supported client</span></span><br/> | <span data-ttu-id="69013-133">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="69013-133">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="69013-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="69013-134">Minimum supported server</span></span><br/> | <span data-ttu-id="69013-135">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="69013-135">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="69013-136">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="69013-136">End of client support</span></span><br/>    | <span data-ttu-id="69013-137">Windows XP</span><span class="sxs-lookup"><span data-stu-id="69013-137">Windows XP</span></span><br/>                                |
| <span data-ttu-id="69013-138">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="69013-138">End of server support</span></span><br/>    | <span data-ttu-id="69013-139">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="69013-139">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="69013-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="69013-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69013-141">**чанжедир**</span><span class="sxs-lookup"><span data-stu-id="69013-141">**ChangeDir**</span></span>](iscardfileaccess-changedir.md)
</dt> <dt>

[<span data-ttu-id="69013-142">**искардфилеакцесс**</span><span class="sxs-lookup"><span data-stu-id="69013-142">**ISCardFileAccess**</span></span>](iscardfileaccess.md)
</dt> </dl>

 

 
