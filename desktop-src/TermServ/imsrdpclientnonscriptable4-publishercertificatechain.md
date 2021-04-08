---
title: IMsRdpClientNonScriptable4 Публишерцертификатечаин, свойство
description: Управляет цепочкой сертификатов издателя. Цепочка хранится в варианте типа VT \_ ByRef, который содержит указатель на \_ структуру контекста цепочки сертификатов \_ . Сведения о \_ структурах VT ByRef см. в разделе Variant и VARIANTARG.
ms.assetid: 27ab0aff-1aef-4701-abe0-849bf32c9773
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Публишерцертификатечаин
- Службы удаленных рабочих столов свойства Публишерцертификатечаин, интерфейс IMsRdpClientNonScriptable4
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable4, свойство Публишерцертификатечаин
- Службы удаленных рабочих столов свойства Публишерцертификатечаин, интерфейс IMsRdpClientNonScriptable5
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable5, свойство Публишерцертификатечаин
- Службы удаленных рабочих столов свойства Публишерцертификатечаин, объект MsRdpClient6
- Службы удаленных рабочих столов объекта MsRdpClient6, свойство Публишерцертификатечаин
- Службы удаленных рабочих столов свойства Публишерцертификатечаин, объект MsRdpClient7
- Службы удаленных рабочих столов объекта MsRdpClient7, свойство Публишерцертификатечаин
- Службы удаленных рабочих столов свойства Публишерцертификатечаин, объект MsRdpClient8
- Службы удаленных рабочих столов объекта MsRdpClient8, свойство Публишерцертификатечаин
- Службы удаленных рабочих столов свойства Публишерцертификатечаин, объект MsRdpClient9
- Службы удаленных рабочих столов объекта MsRdpClient9, свойство Публишерцертификатечаин
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4.PublisherCertificateChain
- IMsRdpClientNonScriptable4.get_PublisherCertificateChain
- IMsRdpClientNonScriptable4.put_PublisherCertificateChain
- IMsRdpClientNonScriptable5.PublisherCertificateChain
- IMsRdpClientNonScriptable5.get_PublisherCertificateChain
- IMsRdpClientNonScriptable5.put_PublisherCertificateChain
- MsRdpClient6.PublisherCertificateChain
- MsRdpClient7.PublisherCertificateChain
- MsRdpClient8.PublisherCertificateChain
- MsRdpClient9.PublisherCertificateChain
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7552483c2fc651ace1a9401e0555f90fb2584423
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892205"
---
# <a name="imsrdpclientnonscriptable4publishercertificatechain-property"></a>IMsRdpClientNonScriptable4: свойство Ублишерцертификатечаин:P

Управляет цепочкой сертификатов издателя. Цепочка хранится в варианте типа **VT \_ ByRef** , который содержит указатель на структуру [**\_ \_ контекста цепочки сертификатов**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_context) . Сведения о структурах **VT \_ ByRef** см. в разделе [Variant и VARIANTARG](/windows/win32/api/oaidl/ns-oaidl-variant).

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_PublisherCertificateChain(
  [in]  VARIANT *pVarCert
);

HRESULT get_PublisherCertificateChain(
  [out] VARIANT *pVarCert
);
```



## <a name="property-value"></a>Значение свойства

Задает цепочку сертификатов издателя. Цепочка хранится в варианте типа **VT \_ ByRef** , который содержит указатель на структуру [**\_ \_ контекста цепочки сертификатов**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_context) .

## <a name="error-codes"></a>Коды ошибок

При успешном выполнении возвращает значение **\_ ОК** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                 |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                           |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| IID<br/>                      | IMsRdpClientNonScriptable4 определяется как f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> <dt>

[**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md)
</dt> </dl>

 

