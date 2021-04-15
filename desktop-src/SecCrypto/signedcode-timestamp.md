---
description: Создает подпись метки времени Authenticode для подписанного исполняемого файла, указанного в свойстве Сигнедкоде. FileName.
ms.assetid: 8f4c9901-b509-4e4c-82f9-a802b0896a11
title: Сигнедкоде. timestamp, метод
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode.Timestamp
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 1b0f4478e4ece5188a96257a8a1dcc9722caa140
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688797"
---
# <a name="signedcodetimestamp-method"></a><span data-ttu-id="314d8-103">Сигнедкоде. timestamp, метод</span><span class="sxs-lookup"><span data-stu-id="314d8-103">SignedCode.Timestamp method</span></span>

<span data-ttu-id="314d8-104">\[Метод **timestamp** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="314d8-104">\[The **Timestamp** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="314d8-105">Вместо этого используйте службы вызова платформы (PInvoke) для вызова функций Win32 API [**сигнерсигнекс**](signersignex.md), [**сигнертиместампекс**](signertimestampex.md)и [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) для подписи содержимого цифровой подписью Authenticode.</span><span class="sxs-lookup"><span data-stu-id="314d8-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md), and [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) functions to sign content with an Authenticode digital signature.</span></span> <span data-ttu-id="314d8-106">Дополнительные сведения о PInvoke см. в разделе [учебник по вызову неуправляемого](https://msdn.microsoft.com/library/aa288468.aspx)кода.</span><span class="sxs-lookup"><span data-stu-id="314d8-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="314d8-107">[.NET и CryptoAPI через p/Invoke: часть 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) и [.NET и CryptoAPI через p/Invoke: часть 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) подразделы [расширения шифрования .NET с помощью CAPICOM и P/Invoke](/previous-versions/ms867087(v=msdn.10)) также могут быть полезными.\]</span><span class="sxs-lookup"><span data-stu-id="314d8-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="314d8-108">Метод **timestamp** создает подпись метки времени Authenticode для подписанного исполняемого файла, указанного в свойстве **сигнедкоде. filename** .</span><span class="sxs-lookup"><span data-stu-id="314d8-108">The **Timestamp** method creates an Authenticode time stamp signature on the signed executable file specified in the **SignedCode.FileName** property.</span></span> <span data-ttu-id="314d8-109">Эта метка времени представляет собой подпись счетчика для подписанного исполняемого файла, которая выполняется центром меток времени.</span><span class="sxs-lookup"><span data-stu-id="314d8-109">This time stamp is a counter signature on the signed executable file that is performed by a time stamp authority.</span></span>

## <a name="syntax"></a><span data-ttu-id="314d8-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="314d8-110">Syntax</span></span>


```VB
SignedCode.Timestamp( _
  ByVal URL _
)
```



## <a name="parameters"></a><span data-ttu-id="314d8-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="314d8-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="314d8-112">*URL-адрес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="314d8-112">*URL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="314d8-113">Строка, содержащая URL-адрес сервера отметок времени.</span><span class="sxs-lookup"><span data-stu-id="314d8-113">A string that contains the URL of the time stamp server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="314d8-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="314d8-114">Return value</span></span>

<span data-ttu-id="314d8-115">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="314d8-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="314d8-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="314d8-116">Remarks</span></span>

<span data-ttu-id="314d8-117">Отметка времени расширяет допустимость сертификата, проверяя, подписан ли исполняемый файл на время отметки времени.</span><span class="sxs-lookup"><span data-stu-id="314d8-117">A time stamp extends the validity of a certificate by verifying that the executable file was signed at the time that it was time stamped.</span></span>

<span data-ttu-id="314d8-118">Перед вызовом этого метода подписанный исполняемый файл должен быть указан в свойстве **сигнедкоде. filename** , а для подписывания исполняемого файла должен быть вызван метод [**сигнедкоде. Sign**](signedcode-sign.md) .</span><span class="sxs-lookup"><span data-stu-id="314d8-118">Before this method can be called, the signed executable file to be time stamped must be specified in the **SignedCode.FileName** property, and the [**SignedCode.Sign**](signedcode-sign.md) method must be called to sign the executable file.</span></span>

<span data-ttu-id="314d8-119">Если подписанный исполняемый файл уже имеет отметку времени, этот метод перезаписывает существующую метку времени.</span><span class="sxs-lookup"><span data-stu-id="314d8-119">If the signed executable file is already time stamped, this method overwrites the existing time stamp.</span></span>

## <a name="requirements"></a><span data-ttu-id="314d8-120">Требования</span><span class="sxs-lookup"><span data-stu-id="314d8-120">Requirements</span></span>



| <span data-ttu-id="314d8-121">Требование</span><span class="sxs-lookup"><span data-stu-id="314d8-121">Requirement</span></span> | <span data-ttu-id="314d8-122">Значение</span><span class="sxs-lookup"><span data-stu-id="314d8-122">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="314d8-123">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="314d8-123">Redistributable</span></span><br/> | <span data-ttu-id="314d8-124">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="314d8-124">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="314d8-125">DLL</span><span class="sxs-lookup"><span data-stu-id="314d8-125">DLL</span></span><br/>             | <dl> <span data-ttu-id="314d8-126"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="314d8-126"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="314d8-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="314d8-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="314d8-128">**сигнедкоде**</span><span class="sxs-lookup"><span data-stu-id="314d8-128">**SignedCode**</span></span>](signedcode.md)
</dt> </dl>

 

 
