---
title: IMsRdpClient2 Коннектедстатустекст, свойство
description: Содержит текст, отображаемый в клиентской области элемента управления, когда элемент управления находится в подключенном состоянии.
ms.assetid: c3d8433b-2fb0-413d-88a3-667149f858ba
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Коннектедстатустекст
- Службы удаленных рабочих столов свойства Коннектедстатустекст, интерфейс IMsRdpClient2
- Службы удаленных рабочих столов интерфейса IMsRdpClient2, свойство Коннектедстатустекст
- Службы удаленных рабочих столов свойства Коннектедстатустекст, интерфейс IMsRdpClient3
- Службы удаленных рабочих столов интерфейса IMsRdpClient3, свойство Коннектедстатустекст
- Службы удаленных рабочих столов свойства Коннектедстатустекст, интерфейс IMsRdpClient4
- Службы удаленных рабочих столов интерфейса IMsRdpClient4, свойство Коннектедстатустекст
- Службы удаленных рабочих столов свойства Коннектедстатустекст, интерфейс IMsRdpClient5
- Службы удаленных рабочих столов интерфейса IMsRdpClient5, свойство Коннектедстатустекст
- Службы удаленных рабочих столов свойства Коннектедстатустекст, интерфейс IMsRdpClient6
- Службы удаленных рабочих столов интерфейса IMsRdpClient6, свойство Коннектедстатустекст
- Службы удаленных рабочих столов свойства Коннектедстатустекст, интерфейс IMsRdpClient7
- Службы удаленных рабочих столов интерфейса IMsRdpClient7, свойство Коннектедстатустекст
- Службы удаленных рабочих столов свойства Коннектедстатустекст, интерфейс IMsRdpClient8
- Службы удаленных рабочих столов интерфейса IMsRdpClient8, свойство Коннектедстатустекст
- Службы удаленных рабочих столов свойства Коннектедстатустекст, интерфейс IMsRdpClient9
- Службы удаленных рабочих столов интерфейса IMsRdpClient9, свойство Коннектедстатустекст
- Службы удаленных рабочих столов свойства Коннектедстатустекст, интерфейс IMsRdpClient10
- Службы удаленных рабочих столов интерфейса IMsRdpClient10, свойство Коннектедстатустекст
topic_type:
- apiref
api_name:
- IMsRdpClient2.ConnectedStatusText
- IMsRdpClient2.get_ConnectedStatusText
- IMsRdpClient2.put_ConnectedStatusText
- IMsRdpClient3.ConnectedStatusText
- IMsRdpClient3.get_ConnectedStatusText
- IMsRdpClient3.put_ConnectedStatusText
- IMsRdpClient4.ConnectedStatusText
- IMsRdpClient4.get_ConnectedStatusText
- IMsRdpClient4.put_ConnectedStatusText
- IMsRdpClient5.ConnectedStatusText
- IMsRdpClient5.get_ConnectedStatusText
- IMsRdpClient5.put_ConnectedStatusText
- IMsRdpClient6.ConnectedStatusText
- IMsRdpClient6.get_ConnectedStatusText
- IMsRdpClient6.put_ConnectedStatusText
- IMsRdpClient7.ConnectedStatusText
- IMsRdpClient7.get_ConnectedStatusText
- IMsRdpClient7.put_ConnectedStatusText
- IMsRdpClient8.ConnectedStatusText
- IMsRdpClient8.get_ConnectedStatusText
- IMsRdpClient8.put_ConnectedStatusText
- IMsRdpClient9.ConnectedStatusText
- IMsRdpClient9.get_ConnectedStatusText
- IMsRdpClient9.put_ConnectedStatusText
- IMsRdpClient10.ConnectedStatusText
- IMsRdpClient10.get_ConnectedStatusText
- IMsRdpClient10.put_ConnectedStatusText
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fd6ee2ac155aa3fc4873ee1a5eb890774b50978
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681809"
---
# <a name="imsrdpclient2connectedstatustext-property"></a>Свойство IMsRdpClient2:: Коннектедстатустекст

Содержит текст, отображаемый в клиентской области элемента управления, когда элемент управления находится в подключенном состоянии.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_ConnectedStatusText(
  [in]  BSTR newVal
);

HRESULT get_ConnectedStatusText(
  [out] BSTR *pConnectedStatusText
);
```



## <a name="property-value"></a>Значение свойства

Свойство **коннектедстатустекст** содержит текст, отображаемый в клиентской области элемента управления, когда элемент управления находится в состоянии Connected.

## <a name="error-codes"></a>Коды ошибок

В случае успеха возвратите значение **\_ ОК** .

## <a name="remarks"></a>Комментарии

Текст, отображаемый в клиентской области элемента управления, когда элемент управления находится в состоянии Connected. Это текст, видимый, например, когда пользователь переключает элемент управления в полноэкранный режим в веб-браузере, сценарий, который оставляет часть элемента управления, размещенного в браузере.

Метод **Get \_ коннектедстатустекст** выделяет память, необходимую для буфера, на который указывает параметр *пконнектедстатустекст* . Вызов приложений C/C++ должен освободить память с помощью вызова функции [**сисфристринг**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) . Это не является обязательным для Visual Basic и скриптов клиентов.

Это свойство не может быть задано, если элемент управления подключен. Проверить, подключен ли элемент управления, можно с помощью метода [**имстскакс:: Get \_ Connected**](imstscax-connected.md) .

Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                               |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                         |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpClient2 определен как e7e17dc4-3b71-4ba7-a8e6-281ffadca28f<br/>       |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**IMsRdpClient2**](imsrdpclient2.md)
</dt> <dt>

[**IMsRdpClient3**](imsrdpclient3.md)
</dt> <dt>

[**IMsRdpClient4**](imsrdpclient4.md)
</dt> <dt>

[**IMsRdpClient5**](imsrdpclient5.md)
</dt> <dt>

[**IMsRdpClient6**](imsrdpclient6.md)
</dt> <dt>

[**IMsRdpClient7**](imsrdpclient7.md)
</dt> <dt>

[**IMsRdpClient8**](imsrdpclient8.md)
</dt> <dt>

[**IMsRdpClient9**](imsrdpclient9.md)
</dt> <dt>

[**IMsRdpClient10**](imsrdpclient10.md)
</dt> </dl>

 

