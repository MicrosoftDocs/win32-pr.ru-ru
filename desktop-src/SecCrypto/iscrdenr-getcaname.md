---
description: Возвращает имя указанного центра сертификации (ЦС) для данного шаблона сертификата.
ms.assetid: e921710a-7c74-4fda-91e1-fbad45889984
title: 'Метод Искрденр:: Жетканаме'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getCAName
- SCrdEnr.getCAName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: b62b0a7e871a29ff0a8edd28eb8cd5e18e97c1a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272261"
---
# <a name="iscrdenrgetcaname-method"></a><span data-ttu-id="5b3ab-103">Метод Искрденр:: Жетканаме</span><span class="sxs-lookup"><span data-stu-id="5b3ab-103">ISCrdEnr::getCAName method</span></span>

<span data-ttu-id="5b3ab-104">Метод **жетканаме** извлекает имя указанного [*центра сертификации*](../secgloss/c-gly.md) (CA) для данного шаблона сертификата.</span><span class="sxs-lookup"><span data-stu-id="5b3ab-104">The **getCAName** method retrieves the name of the specified [*certification authority*](../secgloss/c-gly.md) (CA) for a given certificate template.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b3ab-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5b3ab-105">Syntax</span></span>


```C++
HRESULT getCAName(
  [in]  DWORD     dwFlags,
  [in]  BSTR     bstrCertTemplateName,
  [out] BSTR *pbstrCAName
);
```


```VB

SCrdEnr.getCAName( _
  ByVal dwFlags, _
  ByVal bstrCertTemplateName, _
  ByRef pbstrCAName _
)
```





## <a name="parameters"></a><span data-ttu-id="5b3ab-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5b3ab-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b3ab-107">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5b3ab-107">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b3ab-108">Значение, определяющее, относится ли имя к имени центра сертификации или имени компьютера ЦС.</span><span class="sxs-lookup"><span data-stu-id="5b3ab-108">A value that determines whether the name refers to the CA name or the CA's machine name.</span></span> <span data-ttu-id="5b3ab-109">Если это значение равно бросить \_ Регистрация \_ \_ имени компьютера ЦС \_ (определено как 0x01), то имя будет ссылаться на имя компьютера центра сертификации; в противном случае имя будет ссылаться на имя ЦС.</span><span class="sxs-lookup"><span data-stu-id="5b3ab-109">If this value is SCARD\_ENROLL\_CA\_MACHINE\_NAME (defined as 0x01) then the name refers to the CA's machine name; otherwise the name refers to the CA name.</span></span>

</dd> <dt>

<span data-ttu-id="5b3ab-110">*бстрцерттемплатенаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5b3ab-110">*bstrCertTemplateName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b3ab-111">Имя шаблона сертификата.</span><span class="sxs-lookup"><span data-stu-id="5b3ab-111">The name of the certificate template.</span></span>

</dd> <dt>

<span data-ttu-id="5b3ab-112">*пбстрканаме* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="5b3ab-112">*pbstrCAName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5b3ab-113">Указатель на строку, которая возвращает имя центра сертификации.</span><span class="sxs-lookup"><span data-stu-id="5b3ab-113">A pointer to a string that returns the name of the CA.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b3ab-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5b3ab-114">Return value</span></span>

### <a name="c"></a><span data-ttu-id="5b3ab-115">C++</span><span class="sxs-lookup"><span data-stu-id="5b3ab-115">C++</span></span>

<span data-ttu-id="5b3ab-116">Если метод завершается успешно, метод возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="5b3ab-116">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="5b3ab-117">Если метод завершается с ошибкой, возвращается значение **HRESULT** , указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="5b3ab-117">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="5b3ab-118">Список распространенных кодов ошибок см. в разделе [Общие значения HRESULT](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="5b3ab-118">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

### <a name="vb"></a><span data-ttu-id="5b3ab-119">VB</span><span class="sxs-lookup"><span data-stu-id="5b3ab-119">VB</span></span>

<span data-ttu-id="5b3ab-120">Строка, представляющая имя центра сертификации.</span><span class="sxs-lookup"><span data-stu-id="5b3ab-120">A string that represents the name of the CA.</span></span>

## <a name="remarks"></a><span data-ttu-id="5b3ab-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5b3ab-121">Remarks</span></span>

<span data-ttu-id="5b3ab-122">Имя ЦС по умолчанию — это первое имя в списке доступных центров сертификации.</span><span class="sxs-lookup"><span data-stu-id="5b3ab-122">The default CA name is the first name in the available list of CAs.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b3ab-123">Требования</span><span class="sxs-lookup"><span data-stu-id="5b3ab-123">Requirements</span></span>



| <span data-ttu-id="5b3ab-124">Требование</span><span class="sxs-lookup"><span data-stu-id="5b3ab-124">Requirement</span></span> | <span data-ttu-id="5b3ab-125">Значение</span><span class="sxs-lookup"><span data-stu-id="5b3ab-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5b3ab-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5b3ab-126">Minimum supported client</span></span><br/> | <span data-ttu-id="5b3ab-127">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="5b3ab-127">None supported</span></span><br/>                                                               |
| <span data-ttu-id="5b3ab-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5b3ab-128">Minimum supported server</span></span><br/> | <span data-ttu-id="5b3ab-129">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5b3ab-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5b3ab-130">DLL</span><span class="sxs-lookup"><span data-stu-id="5b3ab-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5b3ab-131"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5b3ab-131"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="5b3ab-132">IID</span><span class="sxs-lookup"><span data-stu-id="5b3ab-132">IID</span></span><br/>                      | <span data-ttu-id="5b3ab-133">IID \_ искрденр определен как 753988a1-1357-436d-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="5b3ab-133">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="5b3ab-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5b3ab-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b3ab-135">**искрденр**</span><span class="sxs-lookup"><span data-stu-id="5b3ab-135">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="5b3ab-136">**Искрденр:: Енумканаме**</span><span class="sxs-lookup"><span data-stu-id="5b3ab-136">**ISCrdEnr::enumCAName**</span></span>](iscrdenr-enumcaname.md)
</dt> <dt>

[<span data-ttu-id="5b3ab-137">**Искрденр:: Жеткакаунт**</span><span class="sxs-lookup"><span data-stu-id="5b3ab-137">**ISCrdEnr::getCACount**</span></span>](iscrdenr-getcacount.md)
</dt> <dt>

[<span data-ttu-id="5b3ab-138">**Искрденр:: Сетканаме**</span><span class="sxs-lookup"><span data-stu-id="5b3ab-138">**ISCrdEnr::setCAName**</span></span>](iscrdenr-setcaname.md)
</dt> </dl>

 

 
