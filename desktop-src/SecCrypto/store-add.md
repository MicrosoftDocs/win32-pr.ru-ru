---
description: Добавляет объект сертификата в открытое хранилище сертификатов.
ms.assetid: 787b8a41-dcdb-4b5b-a1fd-f5424300361b
title: Метод Store. Add
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Add
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 6d217c784fa5f994e88ee2de78f2e1944091d724
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668903"
---
# <a name="storeadd-method"></a><span data-ttu-id="f17da-103">Метод Store. Add</span><span class="sxs-lookup"><span data-stu-id="f17da-103">Store.Add method</span></span>

<span data-ttu-id="f17da-104">\[Метод **Add** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="f17da-104">\[The **Add** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="f17da-105">Вместо этого используйте [**класс X509Store**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="f17da-105">Instead, use the [**X509Store Class**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="f17da-106">Метод **Add** добавляет объект [**сертификата**](certificate.md) в открытое [*хранилище сертификатов*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="f17da-106">The **Add** method adds a [**Certificate**](certificate.md) object to an open [*certificate store*](../secgloss/c-gly.md).</span></span> <span data-ttu-id="f17da-107">Этот метод можно использовать только с хранилищем, которое было открыто с разрешением на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="f17da-107">This method can only be used with a store that has been opened with read/write permission.</span></span>

## <a name="syntax"></a><span data-ttu-id="f17da-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f17da-108">Syntax</span></span>


```VB
Store.Add( _
  ByVal Certificate _
)
```



## <a name="parameters"></a><span data-ttu-id="f17da-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="f17da-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f17da-110">*Сертификат* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f17da-110">*Certificate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f17da-111">Выражение, которое разрешается в объект [**сертификата**](certificate.md) для добавления в хранилище.</span><span class="sxs-lookup"><span data-stu-id="f17da-111">Expression that resolves to a [**Certificate**](certificate.md) object to be added to the store.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f17da-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f17da-112">Return value</span></span>

<span data-ttu-id="f17da-113">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="f17da-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f17da-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f17da-114">Remarks</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f17da-115">При вызове этого метода в системном хранилище из веб-скрипта сценарий должен получить доступ к цифровым сертификатам на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="f17da-115">When this method is called on a system store from a web script, the script needs to access digital certificates on the local computer.</span></span> <span data-ttu-id="f17da-116">Если разрешить сценарию доступ к цифровым сертификатам, веб-сайт, с которого выполняется сценарий, также будет получать доступ к личным сведениям, хранящимся в сертификатах.</span><span class="sxs-lookup"><span data-stu-id="f17da-116">If you allow the script to access your digital certificates, the website from which the script is run will also gain access to any personal information stored in the certificates.</span></span> <span data-ttu-id="f17da-117">При первом вызове этого метода из определенного домена создается диалоговое окно, в котором пользователь должен указать, следует ли разрешить доступ к сертификатам.</span><span class="sxs-lookup"><span data-stu-id="f17da-117">The first time this method is called from a particular domain, a dialog box is generated in which the user must indicate whether access to the certificates should be allowed.</span></span>

 

<span data-ttu-id="f17da-118">Если хранилище не открыто в режиме чтения и записи, этот метод завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="f17da-118">If the store is not open in read/write mode, this method fails.</span></span> <span data-ttu-id="f17da-119">Несмотря на то, что этот метод можно использовать с хранилищами памяти, любые изменения, внесенные в хранилище памяти, не сохраняются при закрытии хранилища.</span><span class="sxs-lookup"><span data-stu-id="f17da-119">Although this method can be used with memory stores, any changes made to a memory store are not persisted when the store is closed.</span></span>

<span data-ttu-id="f17da-120">Если сертификат, добавляемый в хранилище, совпадает с уже существующим, метод **Add** удаляет существующий сертификат из хранилища, а затем добавляет новый сертификат.</span><span class="sxs-lookup"><span data-stu-id="f17da-120">If the certificate being added to the store is the same as one that is already there, the **Add** method deletes the existing certificate from the store and then adds the new certificate.</span></span> <span data-ttu-id="f17da-121">Новый сертификат наследует свойства от существующего сертификата.</span><span class="sxs-lookup"><span data-stu-id="f17da-121">The new certificate inherits properties from the existing certificate.</span></span>

## <a name="requirements"></a><span data-ttu-id="f17da-122">Требования</span><span class="sxs-lookup"><span data-stu-id="f17da-122">Requirements</span></span>



| <span data-ttu-id="f17da-123">Требование</span><span class="sxs-lookup"><span data-stu-id="f17da-123">Requirement</span></span> | <span data-ttu-id="f17da-124">Значение</span><span class="sxs-lookup"><span data-stu-id="f17da-124">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f17da-125">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="f17da-125">Redistributable</span></span><br/> | <span data-ttu-id="f17da-126">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="f17da-126">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="f17da-127">DLL</span><span class="sxs-lookup"><span data-stu-id="f17da-127">DLL</span></span><br/>             | <dl> <span data-ttu-id="f17da-128"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f17da-128"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f17da-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f17da-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f17da-130">**Магазин**</span><span class="sxs-lookup"><span data-stu-id="f17da-130">**Store**</span></span>](store.md)
</dt> <dt>

[<span data-ttu-id="f17da-131">**Криптографические объекты**</span><span class="sxs-lookup"><span data-stu-id="f17da-131">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
