---
description: В следующем примере показан код для получения и проверки подписанного сообщения. Пример получает буфер подписи и его размер в Сигнатуребуффер и Сигнатуребуфферсизе, а также буфер сообщения и его размер в MessageBuffer и Мессажебуфферсизе.
ms.assetid: 3e71aa0f-d135-4311-96f3-305762543627
title: Проверка сообщения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ebf62be707efcbd3ab3a5eca5345261ca1a0fde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343172"
---
# <a name="verifying-a-message"></a>Проверка сообщения

В следующем примере показан код для получения и проверки подписанного сообщения. Пример получает буфер подписи и его размер в Сигнатуребуффер и Сигнатуребуфферсизе, а также буфер сообщения и его размер в MessageBuffer и Мессажебуфферсизе.

В примере предполагается, что инициализирована переменная **сечандле** с именем фконтекст и структура **сокета** с именем s. Объявления и инициации этих переменных см. в разделе [Использование SSPI с клиентом сокетов Windows](using-sspi-with-a-windows-sockets-client.md) и [Использование SSPI с сервером Windows Sockets](using-sspi-with-a-windows-sockets-server.md). Этот код включает вызовы функций в Secur32. lib, которые должны быть включены в библиотеки ссылок.


```C++
//--------------------------------------------------------------------
//  Declare and initialize local variables.
#include <windows.h>
#include <stdio.h>
#include <sspi.h>

#define SECURITY_WIN32
#define MaxMessageLength 1024
#define BUFSIZ 512

void main()
{
    BYTE MessageBuffer[BUFSIZ];
    BYTE SignatureBuffer[BUFSIZ];
    DWORD MessageBufferSize;
    DWORD SignatureBufferSize;
    SECURITY_STATUS SecStatus;
    SecBufferDesc InputBufferDescriptor;
    SecBuffer InputSecurityToken[2];
    ULONG fQOP;

    //------------------------------------------------------------------
    //    Receive the message.

    if(!(ReceiveMsg(
         s,
         MessageBuffer,
         MaxMessageLength,
         &MessageBufferSize)))
    {
         MyHandleError("Error. Message not received.");
    }

    //------------------------------------------------------------------
    //    Receive the signature.

    if(!(ReceiveMsg(
         s,
         SignatureBuffer,
         MaxMessageLength,
         &SignatureBufferSize)))
    {
         MyHandleError("Error. Signature not received.");
    }

    //------------------------------------------------------------------
    // Build the input buffer descriptor.

    InputBufferDescriptor.cBuffers = 2;
    InputBufferDescriptor.pBuffers = InputSecurityToken;
    InputBufferDescriptor.ulVersion = SECBUFFER_VERSION;

    //-------------------------------------------------------------------
    // Build the security buffer for the message.

    InputSecurityToken[0].BufferType = SECBUFFER_DATA;
    InputSecurityToken[0].cbBuffer = MessageBufferSize;
    InputSecurityToken[0].pvBuffer = MessageBuffer;

    //-------------------------------------------------------------------
    // Build the security buffer for the signature.

    InputSecurityToken[1].BufferType = SECBUFFER_TOKEN;
    InputSecurityToken[1].cbBuffer = SignatureBufferSize;
    InputSecurityToken[1].pvBuffer = SignatureBuffer;

    //--------------------------------------------------------------------
    // Call VerifySignature. 

    SecStatus = VerifySignature(
          &phContext,
          &InputBufferDescriptor,  // input message descriptor
          0,                       // no sequence number
          &fQOP                    // quality of protection
          );
    if(SecStatus == SEC_E_OK)
    {
         printf("The signature verified the message.\n");
    }
    else
         if(SecStatus == SEC_E_MESSAGE_ALTERED)
         {
              printf("The message was altered in transit.\n");
         }
         else
              if(SecStatus == SEC_E_OUT_OF_SEQUENCE )
              {
                  printf("The message is out of sequence.\n");
              }
              else
              {
                  printf("An unknown error occurred in VerifyMessage.\n");
              }
}
```



 

 



