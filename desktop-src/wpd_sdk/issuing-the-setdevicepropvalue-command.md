---
description: Выдача команды Сетдевицепропвалуе
ms.assetid: d5917421-fbd4-477c-b29b-9f983c93cfdb
title: Выдача команды Сетдевицепропвалуе
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8949cbf4fe22662de32c4c07de689fec2e6dbad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712971"
---
# <a name="issuing-the-setdevicepropvalue-command"></a>Выдача команды Сетдевицепропвалуе

В примере в этом разделе вызывается команда **сетдевицепропвалуе** MTP. (Полное описание этой команды и ее параметров см. в [спецификации MTP](https://www.usb.org/sites/default/files/MTPv1_1.zip).)

Поскольку эта команда включает данные (или фазу данных), она больше, чем в предыдущем [примере](issuing-the-getnumobjects-command.md). Команды, включающие фазу данных, можно разбить на три части:

1.  Инициация. приложение инициирует команду, уведомляя устройство о том, что данные ожидаются или ожидаются.
2.  Передача. приложение передает данные (путем записи или чтения данных).
3.  Завершение: приложение (или устройство) сигнализирует, что команда завершена, и извлекает код ответа.

Приведенный выше список преобразуется в следующую последовательность команд:

1.  Команда WPD \_ команды " \_ MTP ext" \_ \_ выполняет \_ команду \_ с \_ данными \_ для \_ записи или \_ команды WPD \_ MTP \_ \_ Execute \_ \_ с \_ данными \_ для \_ чтения.
2.  \_Команда WPD \_ \_ (MTP ext \_ Write Data) \_ или \_ команда WPD \_ MTP \_ ext \_ Read \_ Data.
3.  \_команда WPD \_ \_ \_ передает данные с конца MTP \_ \_ .

В случае с **сетдевицепропвалуе** в примере кода используется следующая последовательность:

1.  \_команда WPD \_ MTP \_ \_ выполнил \_ команду \_ с \_ данными \_ для \_ записи.
2.  \_команда WPD \_ MTP \_ ext \_ Write \_ Data.
3.  \_команда WPD \_ \_ \_ передает данные с конца MTP \_ \_ .

В следующем примере кода показано, как приложение WPD инициирует последовательность команд.


```C++
#include <portabledevice.h>
#include <portabledeviceapi.h>
#include <wpdmtpextensions.h>

HRESULT SetDateTime(IPortableDevice* pDevice, LPCWSTR pwszDateTime)
{
    HRESULT hr = S_OK;
    const WORD PTP_OPCODE_SETDEVICEPROPVALUE = 0x1016; 
    const WORD PTP_DEVICEPROPCODE_DATETIME = 0x5011; 
    const WORD PTP_RESPONSECODE_OK = 0x2001;     // 0x2001 indicates command success

    // Build basic WPD parameters for the command
    CComPtr<IPortableDeviceValues> spParameters;
    if (hr == S_OK)
    {
        hr = CoCreateInstance(CLSID_PortableDeviceValues,
                              NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_IPortableDeviceValues,
                              (VOID**)&spParameters);
    }

    // Use WPD_COMMAND_MTP_EXT_EXECUTE_COMMAND_WITH_DATA_TO_WRITE
    if (hr == S_OK)
    {
        hr = spParameters->SetGuidValue(WPD_PROPERTY_COMMON_COMMAND_CATEGORY, 
                                           WPD_COMMAND_MTP_EXT_EXECUTE_COMMAND_WITH_DATA_TO_WRITE.fmtid);
    }

    if (hr == S_OK)
    {
        hr = spParameters->SetUnsignedIntegerValue(WPD_PROPERTY_COMMON_COMMAND_ID, 
                                              WPD_COMMAND_MTP_EXT_EXECUTE_COMMAND_WITH_DATA_TO_WRITE.pid);
    }

    // Specify the actual MTP op-code to execute here
    if (hr == S_OK)
    {
        hr = spParameters->SetUnsignedIntegerValue(WPD_PROPERTY_MTP_EXT_OPERATION_CODE, 
                                                      (ULONG) PTP_OPCODE_SETDEVICEPROPVALUE);
    }

    // SetDevicePropValue requires the property code as an MTP parameter
    // MTP parameters need to be first put into a PropVariantCollection
    CComPtr<IPortableDevicePropVariantCollection> spMtpParams;
    if (hr == S_OK)
    {
        hr = CoCreateInstance(CLSID_PortableDevicePropVariantCollection,
                                  NULL,
                                  CLSCTX_INPROC_SERVER,
                                  IID_IPortableDevicePropVariantCollection,
                                  (VOID**)&spMtpParams);
    }

    PROPVARIANT pvParam = {0};
    pvParam.vt = VT_UI4;

    // Specify the DateTime property as the MTP parameter
    if (hr == S_OK)
    {
        pvParam.ulVal = PTP_DEVICEPROPCODE_DATETIME;
        hr = spMtpParams->Add(&pvParam);
    }

    // Add MTP parameters collection to our main parameter list
    if (hr == S_OK)
    {
        hr = spParameters->SetIPortableDevicePropVariantCollectionValue(
                                          WPD_PROPERTY_MTP_EXT_OPERATION_PARAMS, spMtpParams);
    }  

    // Figure out the data to send - in this case it will be an MTP string
    BYTE* pbBuffer = NULL;
    DWORD cbBufferSize = 0;
    if (hr == S_OK)
    {
        hr = PackString(pwszDateTime, &pbBuffer, &cbBufferSize);
    }

    // Inform the device how much data will arrive - this is a required parameter
    if (hr == S_OK)
    {
        hr = spParameters->SetUnsignedLargeIntegerValue(WPD_PROPERTY_MTP_EXT_TRANSFER_TOTAL_DATA_SIZE, 
                                                        &cbBufferSize);
    }

    // Send the command to initiate the transfer
    CComPtr<IPortableDeviceValues> spResults;
    if (hr == S_OK)
    {
        hr = pDevice->SendCommand(0, spParameters, &spResults);
    }

    // Check if the driver was able to send the command by interrogating WPD_PROPERTY_COMMON_HRESULT
    HRESULT hrCmd = S_OK;
    if (hr == S_OK)
    {
         hr = spResults->GetErrorValue(WPD_PROPERTY_COMMON_HRESULT, &hrCmd);
    }

    if (hr == S_OK)
    {
        printf("Driver return code (initiating): 0x%08X\n", hrCmd);
        hr = hrCmd;
    }

    // The driver returns a context cookie that we need to use during our data transfer
    LPWSTR pwszCookie = NULL;
    if (hr == S_OK)
    {
         hr = spResults->GetStringValue(WPD_PROPERTY_MTP_EXT_TRANSFER_CONTEXT, &pwszContext);
    }
```



В следующем примере кода показано, как приложение WPD передает данные после того, как оно инициировало команду.


```
   // Use the WPD_COMMAND_MTP_EXT_WRITE_DATA command to send the data
    (void) spParameters->Clear();
    if (hr == S_OK)
    {
        hr = spParameters->SetGuidValue(WPD_PROPERTY_COMMON_COMMAND_CATEGORY, 
                                           WPD_COMMAND_MTP_EXT_WRITE_DATA.fmtid);
    }

    if (hr == S_OK)
    {
        hr = spParameters->SetUnsignedIntegerValue(WPD_PROPERTY_COMMON_COMMAND_ID, 
                                                      WPD_COMMAND_MTP_EXT_WRITE_DATA.pid);
    }

    // Specify the same context that we received earlier
    if (hr == S_OK)
    {
        hr = spParameters->SetStringValue(WPD_PROPERTY_MTP_EXT_TRANSFER_CONTEXT, pwszContext);   
    }

    // Specify the number of bytes that arrive with this command. This allows us to 
    // send the data in chunks if required (multiple WRITE_DATA commands). In this case,    //  send the data in a single chunk
    if (hr == S_OK)
    {
        hr = spParameters->SetUnsignedIntegerValue(WPD_PROPERTY_MTP_EXT_TRANSFER_NUM_BYTES_TO_WRITE, 
                                                   cbBufferSize);
    }

    // Provide the data that needs to be transferred
    if (hr == S_OK)
    {
        hr = spParameters->SetBufferValue(WPD_PROPERTY_MTP_EXT_TRANSFER_DATA, pbBuffer, cbBufferSize);
    }

    // Send the data to the device
    spResults = NULL;
    if (hr == S_OK)
    {
        hr = pDevice->SendCommand(0, spParameters, &spResults);
    }

    // Check if the data was sent successfully by interrogating COMMON_HRESULT
    if (hr == S_OK)
    {
         hr = spResults->GetErrorValue(WPD_PROPERTY_COMMON_HRESULT, &hrCmd);
    }

    if (hr == S_OK)
    {
        printf("Driver return code (sending data): 0x%08X\n", hrCmd);
        hr = hrCmd;
    }

    // The driver informs us about the number of bytes that were actually transferred. Normally this
    // should be the same as the number that we provided.
    DWORD cbBytesWritten = 0;
    if (hr == S_OK)
    {
        hr = spResults->GetUnsignedIntegerValue(WPD_PROPERTY_MTP_EXT_TRANSFER_NUM_BYTES_WRITTEN, 
                                                &cbBytesWritten);
    }
```



В следующем примере кода показано, как приложение получает код ответа с устройства.


```
   // Use the WPD_COMMAND_MTP_EXT_END_DATA_TRANSFER command to signal transfer completion
    (void) spParameters->Clear();
    if (hr == S_OK)
    {
        hr = spParameters->SetGuidValue(WPD_PROPERTY_COMMON_COMMAND_CATEGORY, 
                                           WPD_COMMAND_MTP_EXT_END_DATA_TRANSFER.fmtid);
    }

    if (hr == S_OK)
    {
        hr = spParameters->SetUnsignedIntegerValue(WPD_PROPERTY_COMMON_COMMAND_ID, 
                                                      WPD_COMMAND_MTP_EXT_END_DATA_TRANSFER.pid);
    }

    // Specify the same context that we received earlier
    if (hr == S_OK)
    {
        hr = spParameters->SetStringValue(WPD_PROPERTY_MTP_EXT_TRANSFER_CONTEXT, pwszContext);   
    }

    // Send the completion command
    spResults = NULL;
    if (hr == S_OK)
    {
        hr = pDevice->SendCommand(0, spParameters, &spResults);
    }

    // Check if the driver successfully ended the data transfer
    if (hr == S_OK)
    {
         hr = spResults->GetErrorValue(WPD_PROPERTY_COMMON_HRESULT, &hrCmd);
    }

    if (hr == S_OK)
    {
        printf("Driver return code (ending transfer): 0x%08X\n", hrCmd);
        hr = hrCmd;
    }

    // If the command was executed successfully, check the MTP response code to see if the
    // device can handle the command and the data. Be aware that there is a distinction between the command
    // and the data being successfully sent to the device and the command and data being handled successfully 
    // by the device
    DWORD dwResponseCode;
    if (hr == S_OK)
    {
        hr = spResults->GetUnsignedIntegerValue(WPD_PROPERTY_MTP_EXT_RESPONSE_CODE, &dwResponseCode);
    }

    if (hr == S_OK)
    {
        printf("MTP Response code: 0x%X\n", dwResponseCode);
        hr = (dwResponseCode == (DWORD) PTP_RESPONSECODE_OK) ? S_OK : E_FAIL;
    }

    // If response parameters are present, they will be contained in the WPD_PROPERTY_MTP_EXT_RESPONSE_PARAMS 
    // property. SetDevicePropValue does not return additional response parameters, so skip this code 
    

    // Free up any allocated memory
    CoTaskMemFree(pbBuffer);
    CoTaskMemFree(pwszContext);

    return hr;
}
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Поддержка расширений MTP](supporting-mtp-extensions.md)
</dt> </dl>

 

 



