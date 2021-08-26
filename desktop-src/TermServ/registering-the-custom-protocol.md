---
title: Регистрация диспетчера протокола
description: Необходимо создать хотя бы одну запись значения реестра для диспетчера протоколов, чтобы служба службы удаленных рабочих столов могла создать ее экземпляр.
ms.assetid: 4cc7197b-88f3-4906-9b59-66587f970e2a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f851fe74d7e22a068eccd0d901cab14d754b6b2364611bfdda2aecd68dcf224d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119988794"
---
# <a name="registering-the-protocol-manager"></a>Регистрация диспетчера протокола

Необходимо создать хотя бы одну запись значения реестра для диспетчера протоколов, чтобы служба службы удаленных рабочих столов могла создать ее экземпляр.

## <a name="registry-location"></a>Расположение реестра

Создайте раздел реестра в следующем расположении для каждого прослушивателя ([**иврдспротоколлистенер**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollistener)), используемого протоколом. В этом примере новые ключи прослушивателя называются *MyListener1* и *MyListener2*.

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Control
            Terminal Server
               WinStations
                  RDP-Tcp
                  MyListener1
                  MyListener2
```

Для справки можно просмотреть записи значений в разделе по умолчанию ключа прослушивателя **RDP-TCP** в этом расположении.

## <a name="registry-value-entries"></a>Записи значений реестра

Ключ прослушивателя для протокола должен иметь запись значения с именем **лоадаблепротокол \_ Object** .<dl> <dt>

Тип данных
</dt> <dd>REG_SZ</dd> Интерфейс </dl> of type **REG\_SZ** that contains the CLSID of the protocol manager for that listener. (The protocol manager is a COM server that implements the <a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolmanager">**иврдспротоколманажер**</a> .) Служба службы удаленных рабочих столов использует этот идентификатор CLSID для создания экземпляра диспетчера протоколов для этого прослушивателя после того, как обнаружит прослушиватель в реестре.

Если поставщик протокола использует более одного прослушивателя, то служба службы удаленных рабочих столов создает только один экземпляр диспетчера протокола и использует его для вызова [**креателистенер**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-createlistener) один раз для каждого прослушивателя.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Создание поставщика протокол удаленного рабочего стола](creating-a-custom-remote-protocol.md)
</dt> <dt>

[Последовательность вызовов методов](method-call-sequence.md)
</dt> </dl>

 

 




