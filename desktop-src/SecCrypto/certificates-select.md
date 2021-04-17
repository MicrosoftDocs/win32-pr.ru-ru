---
description: Отображает диалоговое окно для выбора сертификатов и возвращает коллекцию выбранных сертификатов.
ms.assetid: dbf49a4b-6da1-4819-afcd-46db89a00fce
title: 'Метод ICertificates2:: SELECT'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates.Select
- ICertificates2.Select
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: cfd5b1cb5e269c14e05de25262fda711549bf02d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689441"
---
# <a name="icertificates2select-method"></a><span data-ttu-id="7c160-103">Метод ICertificates2:: SELECT</span><span class="sxs-lookup"><span data-stu-id="7c160-103">ICertificates2::Select method</span></span>

<span data-ttu-id="7c160-104">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="7c160-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="7c160-105">Вместо этого используйте [**класс X509Certificate2Collection**](/previous-versions/windows/embedded/hh424013(v=msdn.10)) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="7c160-105">Instead, use the [**X509Certificate2Collection Class**](/previous-versions/windows/embedded/hh424013(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="7c160-106">Метод **SELECT** отображает диалоговое окно для выбора сертификатов и возвращает коллекцию выбранных сертификатов.</span><span class="sxs-lookup"><span data-stu-id="7c160-106">The **Select** method displays a dialog box for selecting certificates and returns a collection of those certificates selected.</span></span> <span data-ttu-id="7c160-107">Этот метод появился в CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="7c160-107">This method was introduced in CAPICOM 2.0.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c160-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7c160-108">Syntax</span></span>


```VB
Certificates.Select( _
  [ ByVal Title ], _
  [ ByVal DisplayString ], _
  [ ByVal bMultiSelect ] _
)
```



## <a name="parameters"></a><span data-ttu-id="7c160-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="7c160-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c160-110">*Название* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="7c160-110">*Title* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7c160-111">Строка, содержащая заголовок для диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="7c160-111">String that contains the title for the dialog box.</span></span> <span data-ttu-id="7c160-112">Значение по умолчанию — пустая строка.</span><span class="sxs-lookup"><span data-stu-id="7c160-112">The default value is an empty string ("").</span></span>

</dd> <dt>

<span data-ttu-id="7c160-113">*DisplayString* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="7c160-113">*DisplayString* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7c160-114">Строка, содержащая текст подсказки, отображаемый в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="7c160-114">String that contains the prompt text displayed with the dialog box.</span></span> <span data-ttu-id="7c160-115">Значение по умолчанию — пустая строка.</span><span class="sxs-lookup"><span data-stu-id="7c160-115">The default value is an empty string ("").</span></span>

</dd> <dt>

<span data-ttu-id="7c160-116">*бмултиселект* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="7c160-116">*bMultiSelect* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7c160-117">Логическое значение, указывающее, может ли пользователь выбрать более одного сертификата.</span><span class="sxs-lookup"><span data-stu-id="7c160-117">Boolean value that indicates whether the user can select more than one certificate.</span></span> <span data-ttu-id="7c160-118">Значение true указывает, что можно выбрать несколько сертификатов с помощью клавиши CTRL или SHIFT.</span><span class="sxs-lookup"><span data-stu-id="7c160-118">True indicates multiple certificates can be selected by using the CTRL or SHIFT key.</span></span> <span data-ttu-id="7c160-119">Значением по умолчанию является false.</span><span class="sxs-lookup"><span data-stu-id="7c160-119">The default value is false.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c160-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7c160-120">Return value</span></span>

<span data-ttu-id="7c160-121">Объект [**Certificates**](certificates.md) , который содержит сертификаты, выбранные из диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="7c160-121">A [**Certificates**](certificates.md) object that contains the certificates selected from the dialog box.</span></span>

<span data-ttu-id="7c160-122">**CAPICOM 2,1:** Возвращаемый объект [**Certificates**](certificates.md) содержит ссылки на сертификаты в коллекции, из которой был сделан выбор.</span><span class="sxs-lookup"><span data-stu-id="7c160-122">**CAPICOM 2.1:** The [**Certificates**](certificates.md) object that is returned contains references to the certificates in the collection from which the selection was made.</span></span> <span data-ttu-id="7c160-123">Все изменения, внесенные в сертификаты в возвращенном объекте **Certificate** , отражаются в этой коллекции.</span><span class="sxs-lookup"><span data-stu-id="7c160-123">Any changes made to the certificates in the returned **Certificates** object are reflected in that collection.</span></span>

<span data-ttu-id="7c160-124">**Capicom 2,0, CAPICOM 2.0.0.1, CAPICOM 2.0.0.2 и CAPICOM 2.0.0.3:** Возвращаемый объект [**Certificates**](certificates.md) содержит копии сертификатов в коллекции, из которой был сделан выбор.</span><span class="sxs-lookup"><span data-stu-id="7c160-124">**CAPICOM 2.0, CAPICOM 2.0.0.1, CAPICOM 2.0.0.2, and CAPICOM 2.0.0.3:** The [**Certificates**](certificates.md) object that is returned contains copies of the certificates in the collection from which the selection was made.</span></span> <span data-ttu-id="7c160-125">Любые изменения, внесенные в сертификаты в возвращенном объекте **Certificates** , не отражаются в этой коллекции.</span><span class="sxs-lookup"><span data-stu-id="7c160-125">Any changes made to the certificates in the returned **Certificates** object are not reflected in that collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c160-126">Требования</span><span class="sxs-lookup"><span data-stu-id="7c160-126">Requirements</span></span>



| <span data-ttu-id="7c160-127">Требование</span><span class="sxs-lookup"><span data-stu-id="7c160-127">Requirement</span></span> | <span data-ttu-id="7c160-128">Значение</span><span class="sxs-lookup"><span data-stu-id="7c160-128">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7c160-129">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="7c160-129">End of client support</span></span><br/> | <span data-ttu-id="7c160-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7c160-130">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="7c160-131">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="7c160-131">End of server support</span></span><br/> | <span data-ttu-id="7c160-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7c160-132">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="7c160-133">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="7c160-133">Redistributable</span></span><br/>       | <span data-ttu-id="7c160-134">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="7c160-134">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="7c160-135">DLL</span><span class="sxs-lookup"><span data-stu-id="7c160-135">DLL</span></span><br/>                   | <dl> <span data-ttu-id="7c160-136"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7c160-136"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
