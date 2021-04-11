---
description: Указывает схему защиты для зашифрованных образцов.
ms.assetid: 04E9F908-C61C-43DC-8CF5-9A629FCDD82C
title: Атрибут MFSampleExtension_Encryption_ProtectionScheme (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de298eb310e1258274a4ce24d49e9b53def38cde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155967"
---
# <a name="mfsampleextension_encryption_protectionscheme-attribute"></a><span data-ttu-id="b06b9-103">\_ \_ Атрибут Протектионсчеме Encryption мфсампликстенсион</span><span class="sxs-lookup"><span data-stu-id="b06b9-103">MFSampleExtension\_Encryption\_ProtectionScheme attribute</span></span>

<span data-ttu-id="b06b9-104">Указывает схему защиты для зашифрованных образцов.</span><span class="sxs-lookup"><span data-stu-id="b06b9-104">Specifies the protection scheme for encrypted samples.</span></span>

## <a name="data-type"></a><span data-ttu-id="b06b9-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="b06b9-105">Data type</span></span>

<span data-ttu-id="b06b9-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="b06b9-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="b06b9-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b06b9-107">Remarks</span></span>

<span data-ttu-id="b06b9-108">Значение этого атрибута является членом перечисления [**мфсамплинкриптионпротектионсчеме**](/windows/win32/api/mfapi/ne-mfapi-mfsampleencryptionprotectionscheme) .</span><span class="sxs-lookup"><span data-stu-id="b06b9-108">The value of this attribute is a member of the [**MFSampleEncryptionProtectionScheme**](/windows/win32/api/mfapi/ne-mfapi-mfsampleencryptionprotectionscheme) enumeration.</span></span> <span data-ttu-id="b06b9-109">В случаях, когда источник мультимедиа основан на MP4, значение устанавливается на основе значения поля **\_ тип схемы** в поле Тип схемы ("счм") в заголовке MP4 ("Moov" или "moof").</span><span class="sxs-lookup"><span data-stu-id="b06b9-109">In cases where the media source is MP4-based, the value is set based off the value of the **scheme\_type** field within the scheme type box (‘schm’) in the MP4 header (‘moov’ or ‘moof’).</span></span>

<span data-ttu-id="b06b9-110">Если для **поля \_ тип схемы** в файле в формате MP4 или Stream задано значение ' Cenc ' или ' cbc1 ', то атрибут **мфсампликстенсион \_ ENCRYPTION \_ Протектионсчеме** должен быть установлен в **\_ схему защиты \_ AES \_** -ввод или **\_ схему защиты \_ CBC** соответственно, и никакие значения не должны быть заданы для [мфсампликстенсион \_ ENCRYPTION \_ криптбитеблокк](mfsampleextension-encryption-cryptbyteblock.md) и [мфсампликстенсион \_ ENCRYPTION \_ SkipByteBlock](mfsampleextension-encryption-skipbyteblock.md).</span><span class="sxs-lookup"><span data-stu-id="b06b9-110">If the **scheme\_type** field in an MP4-based file, or stream, is set to ‘cenc’ or ‘cbc1’, then the **MFSampleExtension\_Encryption\_ProtectionScheme** attribute should be set to **PROTECTION\_SCHEME\_AES\_CTR** or **PROTECTION\_SCHEME\_CBC**, respectively, and no values should be set for [MFSampleExtension\_Encryption\_CryptByteBlock](mfsampleextension-encryption-cryptbyteblock.md) and [MFSampleExtension\_Encryption\_SkipByteBlock](mfsampleextension-encryption-skipbyteblock.md).</span></span>

<span data-ttu-id="b06b9-111">Если для **поля \_ тип схемы** в файле в формате MP4 или Stream задано значение ' ценс ' или ' CBCS ', то атрибут **мфсампликстенсион \_ ENCRYPTION \_ протектионсчеме** должен иметь значение **\_ Схема защиты \_ AES \_** -ввод или **\_ Схема защиты \_ CBC** соответственно, а [мфсампликстенсион \_ ENCRYPTION \_ криптбитеблокк](mfsampleextension-encryption-cryptbyteblock.md) и мфсампликстенсион Encryption SkipByteBlock должны быть заданы с помощью значений в поле "tenc". [ \_ \_](mfsampleextension-encryption-skipbyteblock.md)</span><span class="sxs-lookup"><span data-stu-id="b06b9-111">If the **scheme\_type** field in an MP4-based file, or stream, is set to ‘cens’ or ‘cbcs’, then the **MFSampleExtension\_Encryption\_ProtectionScheme** attribute should be set to **PROTECTION\_SCHEME\_AES\_CTR** or **PROTECTION\_SCHEME\_CBC**, respectively, and [MFSampleExtension\_Encryption\_CryptByteBlock](mfsampleextension-encryption-cryptbyteblock.md) and [MFSampleExtension\_Encryption\_SkipByteBlock](mfsampleextension-encryption-skipbyteblock.md) must be set using the values in the ‘tenc’ box.</span></span>

## <a name="examples"></a><span data-ttu-id="b06b9-112">Примеры</span><span class="sxs-lookup"><span data-stu-id="b06b9-112">Examples</span></span>

<span data-ttu-id="b06b9-113">В следующем примере показано, как задать **\_ \_ протектионсчеме шифрования мфсампликстенсион** и связанные с ними атрибуты **мфсампликстенсион Encryption \_ \_ криптбитеблокк** и **мфсампликстенсион \_ ENCRYPTION \_ SkipByteBlock** .</span><span class="sxs-lookup"><span data-stu-id="b06b9-113">The following example shows how to set the **MFSampleExtension\_Encryption\_ProtectionScheme** and the associated **MFSampleExtension\_Encryption\_CryptByteBlock** and **MFSampleExtension\_Encryption\_SkipByteBlock** attributes.</span></span>


```C++
HRESULT AddEncryptionAttributes(_In_ IMFSample* pSample, _In_ bool fIsEncrypted)
{
      HRESULT hr = S_OK;

      if (fIsEncrypted)
    {
        //Set Encryption Protection Scheme
        hr = pSample->UINT32(MFSampleExtension_Encryption_ProtectionScheme,
            SAMPLE_ENCRYPTION_PROTECTION_SCHEME_AES_CBC);
            if (FAILED(hr))
                return hr;

        //Set the Initialization Vector (IV)
  //(spSampleEncryptionData is omitted from this example for simplicity.) 
        hr = pSample->SetBlob(MFSampleExtension_Encryption_SampleID, 
            (BYTE*)(spSampleEncryptionData->m_pInitializationVector),
            spSampleEncryptionData->m_bIVSize);
            if (FAILED(hr))
                return hr;

        //Set crypt and skip byte blocks for pattern encryption
        hr = pSample->SetUINT32(MFSampleExtension_Encryption_CryptByteBlock, 1);
            if (FAILED(hr))
                return hr;

        hr = pSample->SetUINT32(MFSampleExtension_Encryption_SkipByteBlock, 9);
            if (FAILED(hr))
                return hr;
    }
      return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="b06b9-114">Требования</span><span class="sxs-lookup"><span data-stu-id="b06b9-114">Requirements</span></span>



| <span data-ttu-id="b06b9-115">Требование</span><span class="sxs-lookup"><span data-stu-id="b06b9-115">Requirement</span></span> | <span data-ttu-id="b06b9-116">Значение</span><span class="sxs-lookup"><span data-stu-id="b06b9-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b06b9-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b06b9-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b06b9-118">\[Только для настольных приложений Windows 10 версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="b06b9-118">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="b06b9-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b06b9-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b06b9-120">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="b06b9-120">None supported</span></span><br/>                                                          |
| <span data-ttu-id="b06b9-121">Header</span><span class="sxs-lookup"><span data-stu-id="b06b9-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="b06b9-122"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="b06b9-122"><dt>Mfidl.h</dt></span></span> </dl> |



 

 
