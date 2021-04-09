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
# <a name="bluetooth-and-wsaaddresstostring"></a><span data-ttu-id="dbf45-103">Bluetooth и Всааддресстостринг</span><span class="sxs-lookup"><span data-stu-id="dbf45-103">Bluetooth and WSAAddressToString</span></span>

<span data-ttu-id="dbf45-104">Функция [**всааддресстостринг**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa) Windows Sockets используется для преобразования адреса устройства Bluetooth в строку, которая, в свою очередь, предоставляется функции [**Всалукупсервицебегин**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) через структуру [**всакуерисет**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) при получении сведений о службе устройства.</span><span class="sxs-lookup"><span data-stu-id="dbf45-104">The [**WSAAddressToString**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa) Windows Sockets function is used to convert a Bluetooth Device Address to a string, which is in turn provided to the [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) function via the [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) structure when retrieving device service information.</span></span>

<span data-ttu-id="dbf45-105">Хотя адрес устройства Bluetooth помещается в 20-символьный буфер, функция [**всааддресстостринг**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa) в настоящее время возвращает **Всаефаулт** для адресов устройств Bluetooth, если только буфер и указанное значение *лпдваддрессстрингленгс* не имеют символьную длину 40.</span><span class="sxs-lookup"><span data-stu-id="dbf45-105">While a Bluetooth Device Address fits within a 20 character buffer, the [**WSAAddressToString**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa) function currently returns **WSAEFAULT** for Bluetooth Device Addresses unless the buffer and the specified *lpdwAddressStringLength* value are set to a character length of 40.</span></span>

> [!Note]  
> <span data-ttu-id="dbf45-106">Если [**всааддресстостринг**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa) возвращает **всаефаулт** в результате недостаточного буфера, параметр *лпдваддрессстрингленгс* не обновляется с учетом размера буфера, необходимого для операции.</span><span class="sxs-lookup"><span data-stu-id="dbf45-106">When **WSAEFAULT** is returned by [**WSAAddressToString**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa) as the result of an insufficient buffer, the *lpdwAddressStringLength* parameter is not updated with the buffer size required for the operation.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="dbf45-107">См. также</span><span class="sxs-lookup"><span data-stu-id="dbf45-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dbf45-108">**всааддресстостринг**</span><span class="sxs-lookup"><span data-stu-id="dbf45-108">**WSAAddressToString**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa)
</dt> <dt>

[<span data-ttu-id="dbf45-109">Bluetooth и Всалукупсервицебегин</span><span class="sxs-lookup"><span data-stu-id="dbf45-109">Bluetooth and WSALookupServiceBegin</span></span>](bluetooth-and-wsalookupservicebegin.md)
</dt> <dt>

[<span data-ttu-id="dbf45-110">Bluetooth и ВСАКУЕРИСЕТ</span><span class="sxs-lookup"><span data-stu-id="dbf45-110">Bluetooth and WSAQUERYSET</span></span>](bluetooth-and-wsaqueryset.md)
</dt> </dl>

 

 