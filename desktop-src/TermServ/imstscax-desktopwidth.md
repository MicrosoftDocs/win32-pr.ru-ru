---
title: Имстскакс Десктопвидс, свойство
description: Задает ширину текущего элемента управления в пикселях на начальном удаленном рабочем столе.
ms.assetid: 3b349f6c-d068-4047-b8b5-29d022894729
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Десктопвидс
- Службы удаленных рабочих столов свойства Десктопвидс, интерфейс Имстскакс
- Службы удаленных рабочих столов интерфейса Имстскакс, свойство Десктопвидс
- Службы удаленных рабочих столов свойства Десктопвидс, интерфейс Имсрдпклиент
- Службы удаленных рабочих столов интерфейса Имсрдпклиент, свойство Десктопвидс
- Службы удаленных рабочих столов свойства Десктопвидс, интерфейс IMsRdpClient2
- Службы удаленных рабочих столов интерфейса IMsRdpClient2, свойство Десктопвидс
- Службы удаленных рабочих столов свойства Десктопвидс, интерфейс IMsRdpClient3
- Службы удаленных рабочих столов интерфейса IMsRdpClient3, свойство Десктопвидс
- Службы удаленных рабочих столов свойства Десктопвидс, интерфейс IMsRdpClient4
- Службы удаленных рабочих столов интерфейса IMsRdpClient4, свойство Десктопвидс
- Службы удаленных рабочих столов свойства Десктопвидс, интерфейс IMsRdpClient5
- Службы удаленных рабочих столов интерфейса IMsRdpClient5, свойство Десктопвидс
- Службы удаленных рабочих столов свойства Десктопвидс, интерфейс IMsRdpClient6
- Службы удаленных рабочих столов интерфейса IMsRdpClient6, свойство Десктопвидс
- Службы удаленных рабочих столов свойства Десктопвидс, интерфейс IMsRdpClient7
- Службы удаленных рабочих столов интерфейса IMsRdpClient7, свойство Десктопвидс
- Службы удаленных рабочих столов свойства Десктопвидс, интерфейс IMsRdpClient8
- Службы удаленных рабочих столов интерфейса IMsRdpClient8, свойство Десктопвидс
- Службы удаленных рабочих столов свойства Десктопвидс, интерфейс IMsRdpClient9
- Службы удаленных рабочих столов интерфейса IMsRdpClient9, свойство Десктопвидс
topic_type:
- apiref
api_name:
- IMsTscAx.DesktopWidth
- IMsTscAx.get_DesktopWidth
- IMsTscAx.put_DesktopWidth
- IMsRdpClient.DesktopWidth
- IMsRdpClient.get_DesktopWidth
- IMsRdpClient.put_DesktopWidth
- IMsRdpClient2.DesktopWidth
- IMsRdpClient2.get_DesktopWidth
- IMsRdpClient2.put_DesktopWidth
- IMsRdpClient3.DesktopWidth
- IMsRdpClient3.get_DesktopWidth
- IMsRdpClient3.put_DesktopWidth
- IMsRdpClient4.DesktopWidth
- IMsRdpClient4.get_DesktopWidth
- IMsRdpClient4.put_DesktopWidth
- IMsRdpClient5.DesktopWidth
- IMsRdpClient5.get_DesktopWidth
- IMsRdpClient5.put_DesktopWidth
- IMsRdpClient6.DesktopWidth
- IMsRdpClient6.get_DesktopWidth
- IMsRdpClient6.put_DesktopWidth
- IMsRdpClient7.DesktopWidth
- IMsRdpClient7.get_DesktopWidth
- IMsRdpClient7.put_DesktopWidth
- IMsRdpClient8.DesktopWidth
- IMsRdpClient8.get_DesktopWidth
- IMsRdpClient8.put_DesktopWidth
- IMsRdpClient9.DesktopWidth
- IMsRdpClient9.get_DesktopWidth
- IMsRdpClient9.put_DesktopWidth
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca982303208bb2badecf210c9590f627a7b3b57c5acd9ecd7f8fee0bbb70ec93
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119058851"
---
# <a name="imstscaxdesktopwidth-property"></a>Имстскакс: свойство Есктопвидс:D

Задает ширину текущего элемента управления в пикселях на начальном удаленном рабочем столе.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_DesktopWidth(
  [in]  LONG newVal
);

HRESULT get_DesktopWidth(
  [out] LONG *pVal
);
```



## <a name="property-value"></a>Значение свойства

Новая ширина (в пикселях).

## <a name="error-codes"></a>Коды ошибок

В случае успеха возвратите значение **\_ ОК** .

## <a name="remarks"></a>Remarks

задание свойства **десктопвидс** является необязательным, но его необходимо задать перед вызовом метода [**Подключение**](imstscax-connect.md) . Если ширина рабочего стола не указана или имеет значение 0, ширина рабочего стола будет равна ширине элемента управления. Минимальное и максимальное значения зависят от версии операционной системы клиента удаленный рабочий стол.

<dl> <dt>

<span id="_"></span>Windows 8 и Windows Server 2012
</dt> <dd>

200 минимум, максимум 8192

</dd> <dt>

<span id="_"></span>Windows 7/Windows Server 2008
</dt> <dd>

200 минимум, максимум 2048

</dd> <dt>

Windows Vista
</dt> <dd>

200 минимум, максимум 1200

</dd> </dl>

После установки соединения любые изменения ширины элемента управления не изменяют ширину удаленного рабочего стола. Вместо этого элемент управления выводит полосу прокрутки или центрирует удаленный рабочий стол по мере необходимости. Чтобы изменить размер рабочего стола активного подключения, используйте метод [**IMsRdpClient8:: Reconnect**](imsrdpclient8-reconnect.md) .

Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                               |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                         |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ имстскакс определен как 8C11EFAE-92C3-11D1-BC1E-00C04FA31489<br/>            |



## <a name="see-also"></a>См. также

<dl> <dt>

[**имсрдпклиент**](imsrdpclient-interface.md)
</dt> <dt>

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

[**имстскакс**](imstscax-interface.md)
</dt> </dl>

 

 





