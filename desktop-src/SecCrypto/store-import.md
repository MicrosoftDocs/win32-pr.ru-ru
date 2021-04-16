---
description: Метод Import копирует в хранилище Open Certificate содержимое ранее экспортированного хранилища сертификатов. Этот метод можно использовать только с хранилищем, которое было открыто с разрешением на чтение и запись.
ms.assetid: 22db8f1c-469b-4baf-9039-4da35c9c6aa0
title: Метод Store. Import
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Import
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 4eb16cc341eb6e5dcee87216a52e9e3de94d1b65
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648931"
---
# <a name="storeimport-method"></a><span data-ttu-id="2eb62-104">Метод Store. Import</span><span class="sxs-lookup"><span data-stu-id="2eb62-104">Store.Import method</span></span>

<span data-ttu-id="2eb62-105">\[Метод **Import** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="2eb62-105">\[The **Import** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="2eb62-106">Вместо этого используйте [**класс X509Store**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="2eb62-106">Instead, use the [**X509Store Class**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="2eb62-107">Метод **Import** копирует в [*хранилище Open Certificate*](../secgloss/c-gly.md) содержимое ранее экспортированного хранилища сертификатов.</span><span class="sxs-lookup"><span data-stu-id="2eb62-107">The **Import** method copies into an open [*certificate store*](../secgloss/c-gly.md) the contents of a previously exported certificate store.</span></span> <span data-ttu-id="2eb62-108">Этот метод можно использовать только с хранилищем, которое было открыто с разрешением на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="2eb62-108">This method can only be used with a store that has been opened with read/write permission.</span></span>

## <a name="syntax"></a><span data-ttu-id="2eb62-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2eb62-109">Syntax</span></span>


```VB
Store.Import( _
  ByVal EncodedStore _
)
```



## <a name="parameters"></a><span data-ttu-id="2eb62-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="2eb62-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2eb62-111">*Енкодедсторе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2eb62-111">*EncodedStore* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2eb62-112">Строка, содержащая закодированные сертификаты для импорта.</span><span class="sxs-lookup"><span data-stu-id="2eb62-112">The string that contains the encoded certificates to be imported.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2eb62-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2eb62-113">Return value</span></span>

<span data-ttu-id="2eb62-114">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="2eb62-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2eb62-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2eb62-115">Remarks</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2eb62-116">При вызове этого метода из веб-скрипта сценарий должен получить доступ к цифровым сертификатам на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="2eb62-116">When this method is called from a web script, the script needs to access digital certificates on the local computer.</span></span> <span data-ttu-id="2eb62-117">Если разрешить сценарию доступ к цифровым сертификатам, веб-сайт, с которого выполняется сценарий, также будет получать доступ к личным сведениям, хранящимся в сертификатах.</span><span class="sxs-lookup"><span data-stu-id="2eb62-117">If you allow the script to access your digital certificates, the website from which the script is run will also gain access to any personal information stored in the certificates.</span></span> <span data-ttu-id="2eb62-118">При первом вызове этого метода из определенного домена создается диалоговое окно, в котором пользователь должен указать, следует ли разрешить доступ к сертификатам.</span><span class="sxs-lookup"><span data-stu-id="2eb62-118">The first time this method is called from a particular domain, a dialog box is generated in which the user must indicate whether access to the certificates should be allowed.</span></span>

 

<span data-ttu-id="2eb62-119">Если хранилище не открывается с разрешением на чтение и запись, этот метод завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="2eb62-119">If the store is not opened with read/write permission, this method fails.</span></span> <span data-ttu-id="2eb62-120">Несмотря на то, что этот метод можно использовать с хранилищами памяти, любые изменения, внесенные в хранилище памяти, не сохраняются при закрытии хранилища.</span><span class="sxs-lookup"><span data-stu-id="2eb62-120">Although this method can be used with memory stores, any changes made to a memory store are not persisted when the store is closed.</span></span>

## <a name="requirements"></a><span data-ttu-id="2eb62-121">Требования</span><span class="sxs-lookup"><span data-stu-id="2eb62-121">Requirements</span></span>



| <span data-ttu-id="2eb62-122">Требование</span><span class="sxs-lookup"><span data-stu-id="2eb62-122">Requirement</span></span> | <span data-ttu-id="2eb62-123">Значение</span><span class="sxs-lookup"><span data-stu-id="2eb62-123">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2eb62-124">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="2eb62-124">Redistributable</span></span><br/> | <span data-ttu-id="2eb62-125">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="2eb62-125">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="2eb62-126">DLL</span><span class="sxs-lookup"><span data-stu-id="2eb62-126">DLL</span></span><br/>             | <dl> <span data-ttu-id="2eb62-127"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2eb62-127"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2eb62-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2eb62-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2eb62-129">**Магазин**</span><span class="sxs-lookup"><span data-stu-id="2eb62-129">**Store**</span></span>](store.md)
</dt> <dt>

[<span data-ttu-id="2eb62-130">**Криптографические объекты**</span><span class="sxs-lookup"><span data-stu-id="2eb62-130">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
