---
description: Освобождает ключ, хэш или объект поставщика.
ms.assetid: 73fa0a08-4654-4515-bdb2-9951936b689a
title: Функция Сслфриобжект (Сслпровидер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslFreeObject
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: e7d10059942080e7794da7e6b87613189dcf9844
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908827"
---
# <a name="sslfreeobject-function"></a><span data-ttu-id="eaffe-103">Функция Сслфриобжект</span><span class="sxs-lookup"><span data-stu-id="eaffe-103">SslFreeObject function</span></span>

<span data-ttu-id="eaffe-104">Функция **сслфриобжект** освобождает ключ, хэш или объект поставщика.</span><span class="sxs-lookup"><span data-stu-id="eaffe-104">The **SslFreeObject** function frees a key, hash, or provider object.</span></span>

## <a name="syntax"></a><span data-ttu-id="eaffe-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="eaffe-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslFreeObject(
  _In_ NCRYPT_HANDLE hObject,
  _In_ DWORD         dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="eaffe-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="eaffe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eaffe-107">*хобжект* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="eaffe-107">*hObject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eaffe-108">Описатель объекта для освобождения.</span><span class="sxs-lookup"><span data-stu-id="eaffe-108">The handle of the object to free.</span></span>

</dd> <dt>

<span data-ttu-id="eaffe-109">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="eaffe-109">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eaffe-110">Этот параметр зарезервирован для использования в будущем.</span><span class="sxs-lookup"><span data-stu-id="eaffe-110">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eaffe-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="eaffe-111">Return value</span></span>

<span data-ttu-id="eaffe-112">Если функция завершается с ошибкой, она возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="eaffe-112">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="eaffe-113">Если функция завершается ошибкой, она возвращает ненулевое значение ошибки.</span><span class="sxs-lookup"><span data-stu-id="eaffe-113">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="eaffe-114">Возможные коды возврата включают, но не ограничиваются следующим.</span><span class="sxs-lookup"><span data-stu-id="eaffe-114">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="eaffe-115">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="eaffe-115">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="eaffe-116">Описание</span><span class="sxs-lookup"><span data-stu-id="eaffe-116">Description</span></span>                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="eaffe-117">Не <dt>**превышать \_ Недопустимый 0x80090026L \_ Handle**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="eaffe-117"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl>    | <span data-ttu-id="eaffe-118">Недопустимый внутренний маркер.</span><span class="sxs-lookup"><span data-stu-id="eaffe-118">An internal handle is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="eaffe-119"><dt>**Состояние \_ Недопустимый 0xC0000008L \_ Handle**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="eaffe-119"><dt>**STATUS\_INVALID\_HANDLE**</dt> <dt>0xC0000008L</dt></span></span> </dl> | <span data-ttu-id="eaffe-120">Предоставленный маркер недопустим.</span><span class="sxs-lookup"><span data-stu-id="eaffe-120">The provided handle is not valid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="eaffe-121">Требования</span><span class="sxs-lookup"><span data-stu-id="eaffe-121">Requirements</span></span>



| <span data-ttu-id="eaffe-122">Требование</span><span class="sxs-lookup"><span data-stu-id="eaffe-122">Requirement</span></span> | <span data-ttu-id="eaffe-123">Значение</span><span class="sxs-lookup"><span data-stu-id="eaffe-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="eaffe-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="eaffe-124">Minimum supported client</span></span><br/> | <span data-ttu-id="eaffe-125">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="eaffe-125">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="eaffe-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="eaffe-126">Minimum supported server</span></span><br/> | <span data-ttu-id="eaffe-127">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="eaffe-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="eaffe-128">Header</span><span class="sxs-lookup"><span data-stu-id="eaffe-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="eaffe-129"><dt>Сслпровидер. h</dt></span><span class="sxs-lookup"><span data-stu-id="eaffe-129"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="eaffe-130">DLL</span><span class="sxs-lookup"><span data-stu-id="eaffe-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eaffe-131"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eaffe-131"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

 




