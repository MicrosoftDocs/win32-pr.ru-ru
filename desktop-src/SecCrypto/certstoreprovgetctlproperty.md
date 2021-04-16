---
description: Извлекает указанное свойство списка доверия сертификатов (CTL).
ms.assetid: 65309715-65b4-4608-960d-3404e68800a2
title: Функция обратного вызова Цертсторепровжетктлпроперти
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvGetCTLProperty
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: e30a9e735d44fc5681d5cd3932baaf3cc90aa30d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664007"
---
# <a name="certstoreprovgetctlproperty-callback-function"></a><span data-ttu-id="5a475-103">Функция обратного вызова Цертсторепровжетктлпроперти</span><span class="sxs-lookup"><span data-stu-id="5a475-103">CertStoreProvGetCTLProperty callback function</span></span>

<span data-ttu-id="5a475-104">Функция обратного вызова **цертсторепровжетктлпроперти** извлекает указанное свойство [*списка доверия сертификатов*](../secgloss/c-gly.md) (CTL).</span><span class="sxs-lookup"><span data-stu-id="5a475-104">The **CertStoreProvGetCTLProperty** callback function retrieves a specified property of a [*certificate trust list*](../secgloss/c-gly.md) (CTL).</span></span>

## <a name="syntax"></a><span data-ttu-id="5a475-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5a475-105">Syntax</span></span>


```C++
BOOL WINAPI CertStoreProvGetCTLProperty(
  _In_    HCERTSTOREPROV hStoreProv,
  _In_    PCCTL_CONTEXT  pCtlContext,
  _In_    DWORD          dwPropId,
  _In_    DWORD          dwFlags,
  _Out_   void           *pvData,
  _Inout_ DWORD          *pcbData
);
```



## <a name="parameters"></a><span data-ttu-id="5a475-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5a475-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a475-107">*хсторепров* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5a475-107">*hStoreProv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a475-108">**Хцертсторепровный** обработчик [*хранилища сертификатов*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="5a475-108">A **HCERTSTOREPROV** handle to a [*certificate store*](../secgloss/c-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="5a475-109">*пктлконтекст* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5a475-109">*pCtlContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a475-110">Указатель на структуру [**\_ контекста CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) .</span><span class="sxs-lookup"><span data-stu-id="5a475-110">A pointer to a [**CTL\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) structure.</span></span>

</dd> <dt>

<span data-ttu-id="5a475-111">*dwPropId* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5a475-111">*dwPropId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a475-112">Указывает идентификатор свойства.</span><span class="sxs-lookup"><span data-stu-id="5a475-112">Indicates a property identifier.</span></span>

</dd> <dt>

<span data-ttu-id="5a475-113">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5a475-113">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a475-114">Все необходимые значения флагов.</span><span class="sxs-lookup"><span data-stu-id="5a475-114">Any needed flag values.</span></span>

</dd> <dt>

<span data-ttu-id="5a475-115">*пвдата* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="5a475-115">*pvData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5a475-116">Указатель на буфер, содержащий указатель на структуру [**\_ контекста CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) , возвращаемую функцией.</span><span class="sxs-lookup"><span data-stu-id="5a475-116">A pointer to a buffer to contain the pointer to a [**CTL\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) structure to be returned by the function.</span></span> <span data-ttu-id="5a475-117">Чтобы получить значение *пкбдата* перед выделением памяти для буфера, этот параметр можно установить в **значение NULL** при первом вызове функции.</span><span class="sxs-lookup"><span data-stu-id="5a475-117">To get the value of *pcbData* before allocating memory for the buffer, this parameter can be set to **NULL** on a first call to the function.</span></span>

</dd> <dt>

<span data-ttu-id="5a475-118">*пкбдата* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="5a475-118">*pcbData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5a475-119">Указатель на **DWORD** , указывающий длину буфера *пвдата* .</span><span class="sxs-lookup"><span data-stu-id="5a475-119">A pointer to a **DWORD** that indicates the length of the *pvData* buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a475-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5a475-120">Return value</span></span>

<span data-ttu-id="5a475-121">Если функция завершается с ошибкой, функция возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="5a475-121">If the function succeeds, the function returns nonzero.</span></span>

<span data-ttu-id="5a475-122">Если функция завершается ошибкой, она возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="5a475-122">If the function fails, it returns zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a475-123">Требования</span><span class="sxs-lookup"><span data-stu-id="5a475-123">Requirements</span></span>



| <span data-ttu-id="5a475-124">Требование</span><span class="sxs-lookup"><span data-stu-id="5a475-124">Requirement</span></span> | <span data-ttu-id="5a475-125">Значение</span><span class="sxs-lookup"><span data-stu-id="5a475-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5a475-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5a475-126">Minimum supported client</span></span><br/> | <span data-ttu-id="5a475-127">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="5a475-127">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="5a475-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5a475-128">Minimum supported server</span></span><br/> | <span data-ttu-id="5a475-129">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5a475-129">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5a475-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5a475-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a475-131">**\_контекст CTL**</span><span class="sxs-lookup"><span data-stu-id="5a475-131">**CTL\_CONTEXT**</span></span>](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context)
</dt> </dl>

 

 
