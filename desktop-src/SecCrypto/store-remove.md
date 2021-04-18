---
description: Метод Remove удаляет сертификат из открытого хранилища сертификатов. Этот метод можно использовать только с хранилищем, которое было открыто с разрешением на чтение и запись.
ms.assetid: 02bb8ff1-2240-4ec7-b8af-9a7812a12ba9
title: Метод Store. Remove
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Remove
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 188553d6091314e1a872145219ea321d581b35c3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665451"
---
# <a name="storeremove-method"></a><span data-ttu-id="4b4c6-104">Метод Store. Remove</span><span class="sxs-lookup"><span data-stu-id="4b4c6-104">Store.Remove method</span></span>

<span data-ttu-id="4b4c6-105">\[Метод **Remove** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="4b4c6-105">\[The **Remove** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="4b4c6-106">Вместо этого используйте [**класс X509Store**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="4b4c6-106">Instead, use the [**X509Store Class**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="4b4c6-107">Метод **Remove** удаляет [*сертификат*](../secgloss/c-gly.md) из открытого [*хранилища сертификатов*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="4b4c6-107">The **Remove** method removes a [*certificate*](../secgloss/c-gly.md) from an open [*certificate store*](../secgloss/c-gly.md).</span></span> <span data-ttu-id="4b4c6-108">Этот метод можно использовать только с хранилищем, которое было открыто с разрешением на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="4b4c6-108">This method can only be used with a store that has been opened with read/write permission.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b4c6-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4b4c6-109">Syntax</span></span>


```VB
Store.Remove( _
  ByVal Certificate _
)
```



## <a name="parameters"></a><span data-ttu-id="4b4c6-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="4b4c6-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b4c6-111">*Сертификат* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4b4c6-111">*Certificate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b4c6-112">Выражение, которое разрешается в экземпляр объекта [**сертификата**](certificate.md) для удаления из хранилища.</span><span class="sxs-lookup"><span data-stu-id="4b4c6-112">Expression that resolves to an instance of a [**Certificate**](certificate.md) object to be removed from the store.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b4c6-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4b4c6-113">Return value</span></span>

<span data-ttu-id="4b4c6-114">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="4b4c6-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4b4c6-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4b4c6-115">Remarks</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4b4c6-116">При вызове этого метода из веб-скрипта сценарий должен удалить цифровые сертификаты с локального компьютера.</span><span class="sxs-lookup"><span data-stu-id="4b4c6-116">When this method is called from a web script, the script needs to delete digital certificates from the local computer.</span></span> <span data-ttu-id="4b4c6-117">Разрешение удаления цифровых сертификатов недоверенными веб-сайтами является угрозой безопасности.</span><span class="sxs-lookup"><span data-stu-id="4b4c6-117">Allowing untrusted websites to delete digital certificates is a security risk.</span></span> <span data-ttu-id="4b4c6-118">Диалоговое окно, предлагающее, может ли веб-сайт удалять сертификаты, появляется при первом вызове этого метода.</span><span class="sxs-lookup"><span data-stu-id="4b4c6-118">A dialog box that asks whether the website can delete certificates appears when this method is first called.</span></span> <span data-ttu-id="4b4c6-119">Если разрешить приложению удалять сертификаты и установить флажок "больше не выводить это окно", диалоговое окно не будет отображаться для сценариев, удаляющих сертификаты в этом домене.</span><span class="sxs-lookup"><span data-stu-id="4b4c6-119">If you allow the application to delete certificates and select "Do not show this dialog box again," the dialog box will no longer appear for any script that deletes certificates within that domain.</span></span> <span data-ttu-id="4b4c6-120">Однако скрипты за пределами этого домена, которые пытаются удалить сертификаты, по-прежнему приведут к появлению этого диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="4b4c6-120">However, scripts outside that domain that attempt to delete certificates will still cause this dialog box to appear.</span></span> <span data-ttu-id="4b4c6-121">Если вы не разрешите скрипту удалять сертификаты и установите флажок "больше не выводить это диалоговое окно", скрипты в этом домене автоматически не смогут удалять сертификаты.</span><span class="sxs-lookup"><span data-stu-id="4b4c6-121">If you do not allow the script to delete certificates and select "Do not show this dialog box again," scripts within that domain will automatically be refused the ability to delete certificates.</span></span>

 

<span data-ttu-id="4b4c6-122">При удалении сертификата из хранилища сначала необходимо удалить закрытый ключ, связанный с сертификатом.</span><span class="sxs-lookup"><span data-stu-id="4b4c6-122">When you delete a certificate from a store, you should first delete the private key associated with the certificate.</span></span>

<span data-ttu-id="4b4c6-123">Если хранилище не открыто с разрешением на чтение и запись, этот метод завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="4b4c6-123">If the store is not open with read/write permission, this method fails.</span></span> <span data-ttu-id="4b4c6-124">Несмотря на то, что этот метод можно использовать с хранилищами памяти, любые изменения, внесенные в хранилище памяти, не сохраняются при закрытии хранилища.</span><span class="sxs-lookup"><span data-stu-id="4b4c6-124">Although this method can be used with memory stores, any changes made to a memory store are not persisted when the store is closed.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b4c6-125">Требования</span><span class="sxs-lookup"><span data-stu-id="4b4c6-125">Requirements</span></span>



| <span data-ttu-id="4b4c6-126">Требование</span><span class="sxs-lookup"><span data-stu-id="4b4c6-126">Requirement</span></span> | <span data-ttu-id="4b4c6-127">Значение</span><span class="sxs-lookup"><span data-stu-id="4b4c6-127">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4b4c6-128">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="4b4c6-128">Redistributable</span></span><br/> | <span data-ttu-id="4b4c6-129">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="4b4c6-129">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="4b4c6-130">DLL</span><span class="sxs-lookup"><span data-stu-id="4b4c6-130">DLL</span></span><br/>             | <dl> <span data-ttu-id="4b4c6-131"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4b4c6-131"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b4c6-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4b4c6-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b4c6-133">**Магазин**</span><span class="sxs-lookup"><span data-stu-id="4b4c6-133">**Store**</span></span>](store.md)
</dt> <dt>

[<span data-ttu-id="4b4c6-134">**Криптографические объекты**</span><span class="sxs-lookup"><span data-stu-id="4b4c6-134">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
