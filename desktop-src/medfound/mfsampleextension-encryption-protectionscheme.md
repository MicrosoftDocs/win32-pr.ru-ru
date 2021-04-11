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
# <a name="mfsampleextension_encryption_protectionscheme-attribute"></a>\_ \_ Атрибут Протектионсчеме Encryption мфсампликстенсион

Указывает схему защиты для зашифрованных образцов.

## <a name="data-type"></a>Тип данных

**UINT32**

## <a name="remarks"></a>Комментарии

Значение этого атрибута является членом перечисления [**мфсамплинкриптионпротектионсчеме**](/windows/win32/api/mfapi/ne-mfapi-mfsampleencryptionprotectionscheme) . В случаях, когда источник мультимедиа основан на MP4, значение устанавливается на основе значения поля **\_ тип схемы** в поле Тип схемы ("счм") в заголовке MP4 ("Moov" или "moof").

Если для **поля \_ тип схемы** в файле в формате MP4 или Stream задано значение ' Cenc ' или ' cbc1 ', то атрибут **мфсампликстенсион \_ ENCRYPTION \_ Протектионсчеме** должен быть установлен в **\_ схему защиты \_ AES \_** -ввод или **\_ схему защиты \_ CBC** соответственно, и никакие значения не должны быть заданы для [мфсампликстенсион \_ ENCRYPTION \_ криптбитеблокк](mfsampleextension-encryption-cryptbyteblock.md) и [мфсампликстенсион \_ ENCRYPTION \_ SkipByteBlock](mfsampleextension-encryption-skipbyteblock.md).

Если для **поля \_ тип схемы** в файле в формате MP4 или Stream задано значение ' ценс ' или ' CBCS ', то атрибут **мфсампликстенсион \_ ENCRYPTION \_ протектионсчеме** должен иметь значение **\_ Схема защиты \_ AES \_** -ввод или **\_ Схема защиты \_ CBC** соответственно, а [мфсампликстенсион \_ ENCRYPTION \_ криптбитеблокк](mfsampleextension-encryption-cryptbyteblock.md) и мфсампликстенсион Encryption SkipByteBlock должны быть заданы с помощью значений в поле "tenc". [ \_ \_](mfsampleextension-encryption-skipbyteblock.md)

## <a name="examples"></a>Примеры

В следующем примере показано, как задать **\_ \_ протектионсчеме шифрования мфсампликстенсион** и связанные с ними атрибуты **мфсампликстенсион Encryption \_ \_ криптбитеблокк** и **мфсампликстенсион \_ ENCRYPTION \_ SkipByteBlock** .


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



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только для настольных приложений Windows 10 версии 1709\]<br/>                          |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                          |
| Header<br/>                   | <dl> <dt>Мфидл. h</dt> </dl> |



 

 
