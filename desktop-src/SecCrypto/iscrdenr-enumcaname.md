---
description: Перечисляет имена центров сертификации (ЦС) для заданного имени шаблона сертификата.
ms.assetid: 82cc3346-a8b9-4abd-933a-c212a37a373e
title: 'Метод Искрденр:: Енумканаме'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.enumCAName
- SCrdEnr.enumCAName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: c23df2f74cdf3791f1280e38cbff8ddd48f924b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684338"
---
# <a name="iscrdenrenumcaname-method"></a><span data-ttu-id="e8bb7-103">Метод Искрденр:: Енумканаме</span><span class="sxs-lookup"><span data-stu-id="e8bb7-103">ISCrdEnr::enumCAName method</span></span>

<span data-ttu-id="e8bb7-104">Метод **енумканаме** перечисляет имена [*центров сертификации*](../secgloss/c-gly.md) (CAS) для заданного имени шаблона сертификата.</span><span class="sxs-lookup"><span data-stu-id="e8bb7-104">The **enumCAName** method enumerates the name of the [*certification authorities*](../secgloss/c-gly.md) (CAs) for a given certificate template name.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8bb7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e8bb7-105">Syntax</span></span>


```C++
HRESULT enumCAName(
  [in]  DWORD     dwIndex,
  [in]  DWORD     dwFlags,
  [in]  BSTR     bstrCertTemplateName,
  [out] BSTR *pbstrCAName
);
```


```VB

SCrdEnr.enumCAName( _
  ByVal dwIndex, _
  ByVal dwFlags, _
  ByVal bstrCertTemplateName, _
  ByRef pbstrCAName _
)
```





## <a name="parameters"></a><span data-ttu-id="e8bb7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e8bb7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8bb7-107">*двиндекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e8bb7-107">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8bb7-108">Отсчитываемый от нуля индекс последовательности перечисления.</span><span class="sxs-lookup"><span data-stu-id="e8bb7-108">The zero-based index for the enumeration sequence.</span></span>

</dd> <dt>

<span data-ttu-id="e8bb7-109">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e8bb7-109">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8bb7-110">Значение, определяющее, относится ли имя к имени центра сертификации или имени компьютера ЦС.</span><span class="sxs-lookup"><span data-stu-id="e8bb7-110">A value that determines whether the name refers to the CA name or the CA's machine name.</span></span> <span data-ttu-id="e8bb7-111">Если это значение равно бросить \_ Регистрация \_ \_ имени компьютера ЦС \_ (определено как 0x01), имя будет ССЫЛАТЬСЯ на имя компьютера ЦС.</span><span class="sxs-lookup"><span data-stu-id="e8bb7-111">If this value is SCARD\_ENROLL\_CA\_MACHINE\_NAME (defined as 0x01), the name refers to the CA's machine name.</span></span> <span data-ttu-id="e8bb7-112">В противном случае имя ссылается на имя ЦС.</span><span class="sxs-lookup"><span data-stu-id="e8bb7-112">Otherwise the name refers to the CA name.</span></span>

</dd> <dt>

<span data-ttu-id="e8bb7-113">*бстрцерттемплатенаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e8bb7-113">*bstrCertTemplateName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8bb7-114">Имя шаблона сертификата.</span><span class="sxs-lookup"><span data-stu-id="e8bb7-114">The name of the certificate template.</span></span>

</dd> <dt>

<span data-ttu-id="e8bb7-115">*пбстрканаме* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e8bb7-115">*pbstrCAName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e8bb7-116">Указатель на строку, которая возвращает имя центра сертификации.</span><span class="sxs-lookup"><span data-stu-id="e8bb7-116">A pointer to a string that returns the name of the CA.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8bb7-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e8bb7-117">Return value</span></span>

### <a name="c"></a><span data-ttu-id="e8bb7-118">C++</span><span class="sxs-lookup"><span data-stu-id="e8bb7-118">C++</span></span>

<span data-ttu-id="e8bb7-119">Если метод завершается успешно, метод возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="e8bb7-119">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="e8bb7-120">Если метод завершается с ошибкой, возвращается значение **HRESULT** , указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="e8bb7-120">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="e8bb7-121">Список распространенных кодов ошибок см. в разделе [Общие значения HRESULT](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="e8bb7-121">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

### <a name="vb"></a><span data-ttu-id="e8bb7-122">VB</span><span class="sxs-lookup"><span data-stu-id="e8bb7-122">VB</span></span>

<span data-ttu-id="e8bb7-123">Строка, представляющая имя центра сертификации.</span><span class="sxs-lookup"><span data-stu-id="e8bb7-123">A string that represents the name of the CA.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8bb7-124">Требования</span><span class="sxs-lookup"><span data-stu-id="e8bb7-124">Requirements</span></span>



| <span data-ttu-id="e8bb7-125">Требование</span><span class="sxs-lookup"><span data-stu-id="e8bb7-125">Requirement</span></span> | <span data-ttu-id="e8bb7-126">Значение</span><span class="sxs-lookup"><span data-stu-id="e8bb7-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e8bb7-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e8bb7-127">Minimum supported client</span></span><br/> | <span data-ttu-id="e8bb7-128">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="e8bb7-128">None supported</span></span><br/>                                                               |
| <span data-ttu-id="e8bb7-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e8bb7-129">Minimum supported server</span></span><br/> | <span data-ttu-id="e8bb7-130">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e8bb7-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e8bb7-131">DLL</span><span class="sxs-lookup"><span data-stu-id="e8bb7-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e8bb7-132"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e8bb7-132"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="e8bb7-133">IID</span><span class="sxs-lookup"><span data-stu-id="e8bb7-133">IID</span></span><br/>                      | <span data-ttu-id="e8bb7-134">IID \_ искрденр определен как 753988a1-1357-436d-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="e8bb7-134">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="e8bb7-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e8bb7-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8bb7-136">**искрденр**</span><span class="sxs-lookup"><span data-stu-id="e8bb7-136">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="e8bb7-137">**Искрденр:: Жеткакаунт**</span><span class="sxs-lookup"><span data-stu-id="e8bb7-137">**ISCrdEnr::getCACount**</span></span>](iscrdenr-getcacount.md)
</dt> <dt>

[<span data-ttu-id="e8bb7-138">**Искрденр:: Жетканаме**</span><span class="sxs-lookup"><span data-stu-id="e8bb7-138">**ISCrdEnr::getCAName**</span></span>](iscrdenr-getcaname.md)
</dt> <dt>

[<span data-ttu-id="e8bb7-139">**Искрденр:: Сетканаме**</span><span class="sxs-lookup"><span data-stu-id="e8bb7-139">**ISCrdEnr::setCAName**</span></span>](iscrdenr-setcaname.md)
</dt> </dl>

 

 
