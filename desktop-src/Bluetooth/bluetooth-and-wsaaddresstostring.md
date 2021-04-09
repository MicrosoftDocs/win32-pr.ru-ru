---
title: Bluetooth и Всааддресстостринг
description: Функция Всааддресстостринг Windows Sockets используется для преобразования адреса устройства Bluetooth в строку, которая, в свою очередь, предоставляется функции Всалукупсервицебегин через структуру ВСАКУЕРИСЕТ при получении сведений о службе устройства.
ms.assetid: 3489d29a-2b64-4051-b579-57878efc0c73
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a78e8a9ae3ea6a0f853619a3f3610a64204ad3c3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070084"
---
# <a name="bluetooth-and-wsaaddresstostring"></a>Bluetooth и Всааддресстостринг

Функция [**всааддресстостринг**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa) Windows Sockets используется для преобразования адреса устройства Bluetooth в строку, которая, в свою очередь, предоставляется функции [**Всалукупсервицебегин**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) через структуру [**всакуерисет**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) при получении сведений о службе устройства.

Хотя адрес устройства Bluetooth помещается в 20-символьный буфер, функция [**всааддресстостринг**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa) в настоящее время возвращает **Всаефаулт** для адресов устройств Bluetooth, если только буфер и указанное значение *лпдваддрессстрингленгс* не имеют символьную длину 40.

> [!Note]  
> Если [**всааддресстостринг**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa) возвращает **всаефаулт** в результате недостаточного буфера, параметр *лпдваддрессстрингленгс* не обновляется с учетом размера буфера, необходимого для операции.

 

## <a name="related-topics"></a>См. также

<dl> <dt>

[**всааддресстостринг**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa)
</dt> <dt>

[Bluetooth и Всалукупсервицебегин](bluetooth-and-wsalookupservicebegin.md)
</dt> <dt>

[Bluetooth и ВСАКУЕРИСЕТ](bluetooth-and-wsaqueryset.md)
</dt> </dl>

 

 