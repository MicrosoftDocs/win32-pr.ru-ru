---
description: Указывает имя центра сертификации (ЦС).
ms.assetid: 224c2a51-8a25-4b66-b86b-c87531475145
title: 'Метод Искрденр:: Сетканаме'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.setCAName
- SCrdEnr.setCAName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 46dcd9294337c088b9e1b0ab68bddefe4308ed27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664236"
---
# <a name="iscrdenrsetcaname-method"></a><span data-ttu-id="f52e8-103">Метод Искрденр:: Сетканаме</span><span class="sxs-lookup"><span data-stu-id="f52e8-103">ISCrdEnr::setCAName method</span></span>

<span data-ttu-id="f52e8-104">Метод **сетканаме** указывает имя [*центра сертификации*](../secgloss/c-gly.md) (ЦС).</span><span class="sxs-lookup"><span data-stu-id="f52e8-104">The **setCAName** method specifies the name of the [*certification authority*](../secgloss/c-gly.md) (CA).</span></span>

## <a name="syntax"></a><span data-ttu-id="f52e8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f52e8-105">Syntax</span></span>


```C++
HRESULT setCAName(
  [in] DWORD dwFlags,
  [in] BSTR bstrCertTemplateName,
  [in] BSTR bstrCAName
);
```


```VB

SCrdEnr.setCAName( _
  ByVal dwFlags, _
  ByVal bstrCertTemplateName, _
  ByVal bstrCAName _
)
```





## <a name="parameters"></a><span data-ttu-id="f52e8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f52e8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f52e8-107">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f52e8-107">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f52e8-108">Значение, указывающее, относится ли имя к имени центра сертификации или имени компьютера ЦС.</span><span class="sxs-lookup"><span data-stu-id="f52e8-108">Value that specifies whether the name refers to the CA name or the CA's machine name.</span></span> <span data-ttu-id="f52e8-109">Если это значение равно бросить \_ Регистрация \_ \_ имени компьютера ЦС \_ (определено как 0x01), имя будет ССЫЛАТЬСЯ на имя компьютера ЦС.</span><span class="sxs-lookup"><span data-stu-id="f52e8-109">If this value is SCARD\_ENROLL\_CA\_MACHINE\_NAME (defined as 0x01), the name refers to the CA's machine name.</span></span> <span data-ttu-id="f52e8-110">В противном случае имя ссылается на имя ЦС.</span><span class="sxs-lookup"><span data-stu-id="f52e8-110">Otherwise, the name refers to the CA name.</span></span>

</dd> <dt>

<span data-ttu-id="f52e8-111">*бстрцерттемплатенаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f52e8-111">*bstrCertTemplateName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f52e8-112">Имя шаблона сертификата.</span><span class="sxs-lookup"><span data-stu-id="f52e8-112">Name of the certificate template.</span></span>

</dd> <dt>

<span data-ttu-id="f52e8-113">*бстрканаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f52e8-113">*bstrCAName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f52e8-114">Имя ЦС, которое будет использоваться с шаблоном сертификата, указанным параметром *бстрцерттемплатенаме*.</span><span class="sxs-lookup"><span data-stu-id="f52e8-114">CA name to be used with the certificate template specified by *bstrCertTemplateName*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f52e8-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f52e8-115">Return value</span></span>

### <a name="vb"></a><span data-ttu-id="f52e8-116">VB</span><span class="sxs-lookup"><span data-stu-id="f52e8-116">VB</span></span>

<span data-ttu-id="f52e8-117">Возвращаемое значение является значением **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="f52e8-117">The return value is an **HRESULT**.</span></span> <span data-ttu-id="f52e8-118">Значение S \_ ОК указывает, что вызов выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="f52e8-118">A value of S\_OK indicates that the call was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="f52e8-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f52e8-119">Remarks</span></span>

<span data-ttu-id="f52e8-120">Используйте этот метод, чтобы указать ЦС для шаблона сертификата.</span><span class="sxs-lookup"><span data-stu-id="f52e8-120">Use this method to specify a CA for a certificate template.</span></span>

## <a name="requirements"></a><span data-ttu-id="f52e8-121">Требования</span><span class="sxs-lookup"><span data-stu-id="f52e8-121">Requirements</span></span>



| <span data-ttu-id="f52e8-122">Требование</span><span class="sxs-lookup"><span data-stu-id="f52e8-122">Requirement</span></span> | <span data-ttu-id="f52e8-123">Значение</span><span class="sxs-lookup"><span data-stu-id="f52e8-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f52e8-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f52e8-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f52e8-125">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="f52e8-125">None supported</span></span><br/>                                                               |
| <span data-ttu-id="f52e8-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f52e8-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f52e8-127">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f52e8-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f52e8-128">DLL</span><span class="sxs-lookup"><span data-stu-id="f52e8-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f52e8-129"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f52e8-129"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="f52e8-130">IID</span><span class="sxs-lookup"><span data-stu-id="f52e8-130">IID</span></span><br/>                      | <span data-ttu-id="f52e8-131">IID \_ искрденр определен как 753988a1-1357-436d-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="f52e8-131">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="f52e8-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f52e8-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f52e8-133">**искрденр**</span><span class="sxs-lookup"><span data-stu-id="f52e8-133">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="f52e8-134">**Искрденр:: Енумканаме**</span><span class="sxs-lookup"><span data-stu-id="f52e8-134">**ISCrdEnr::enumCAName**</span></span>](iscrdenr-enumcaname.md)
</dt> <dt>

[<span data-ttu-id="f52e8-135">**Искрденр:: Жетканаме**</span><span class="sxs-lookup"><span data-stu-id="f52e8-135">**ISCrdEnr::getCAName**</span></span>](iscrdenr-getcaname.md)
</dt> </dl>

 

 
