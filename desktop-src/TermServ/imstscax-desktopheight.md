---
title: Имстскакс Десктофеигхт, свойство
description: Задает высоту текущего элемента управления в пикселях на начальном удаленном рабочем столе.
ms.assetid: 7071053b-bdd1-408b-ab69-965c504fafb0
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Десктофеигхт
- Службы удаленных рабочих столов свойства Десктофеигхт, интерфейс Имстскакс
- Службы удаленных рабочих столов интерфейса Имстскакс, свойство Десктофеигхт
- Службы удаленных рабочих столов свойства Десктофеигхт, интерфейс Имсрдпклиент
- Службы удаленных рабочих столов интерфейса Имсрдпклиент, свойство Десктофеигхт
- Службы удаленных рабочих столов свойства Десктофеигхт, интерфейс IMsRdpClient2
- Службы удаленных рабочих столов интерфейса IMsRdpClient2, свойство Десктофеигхт
- Службы удаленных рабочих столов свойства Десктофеигхт, интерфейс IMsRdpClient3
- Службы удаленных рабочих столов интерфейса IMsRdpClient3, свойство Десктофеигхт
- Службы удаленных рабочих столов свойства Десктофеигхт, интерфейс IMsRdpClient4
- Службы удаленных рабочих столов интерфейса IMsRdpClient4, свойство Десктофеигхт
- Службы удаленных рабочих столов свойства Десктофеигхт, интерфейс IMsRdpClient5
- Службы удаленных рабочих столов интерфейса IMsRdpClient5, свойство Десктофеигхт
- Службы удаленных рабочих столов свойства Десктофеигхт, интерфейс IMsRdpClient6
- Службы удаленных рабочих столов интерфейса IMsRdpClient6, свойство Десктофеигхт
- Службы удаленных рабочих столов свойства Десктофеигхт, интерфейс IMsRdpClient7
- Службы удаленных рабочих столов интерфейса IMsRdpClient7, свойство Десктофеигхт
- Службы удаленных рабочих столов свойства Десктофеигхт, интерфейс IMsRdpClient8
- Службы удаленных рабочих столов интерфейса IMsRdpClient8, свойство Десктофеигхт
- Службы удаленных рабочих столов свойства Десктофеигхт, интерфейс IMsRdpClient9
- Службы удаленных рабочих столов интерфейса IMsRdpClient9, свойство Десктофеигхт
topic_type:
- apiref
api_name:
- IMsTscAx.DesktopHeight
- IMsTscAx.get_DesktopHeight
- IMsTscAx.put_DesktopHeight
- IMsRdpClient.DesktopHeight
- IMsRdpClient.get_DesktopHeight
- IMsRdpClient.put_DesktopHeight
- IMsRdpClient2.DesktopHeight
- IMsRdpClient2.get_DesktopHeight
- IMsRdpClient2.put_DesktopHeight
- IMsRdpClient3.DesktopHeight
- IMsRdpClient3.get_DesktopHeight
- IMsRdpClient3.put_DesktopHeight
- IMsRdpClient4.DesktopHeight
- IMsRdpClient4.get_DesktopHeight
- IMsRdpClient4.put_DesktopHeight
- IMsRdpClient5.DesktopHeight
- IMsRdpClient5.get_DesktopHeight
- IMsRdpClient5.put_DesktopHeight
- IMsRdpClient6.DesktopHeight
- IMsRdpClient6.get_DesktopHeight
- IMsRdpClient6.put_DesktopHeight
- IMsRdpClient7.DesktopHeight
- IMsRdpClient7.get_DesktopHeight
- IMsRdpClient7.put_DesktopHeight
- IMsRdpClient8.DesktopHeight
- IMsRdpClient8.get_DesktopHeight
- IMsRdpClient8.put_DesktopHeight
- IMsRdpClient9.DesktopHeight
- IMsRdpClient9.get_DesktopHeight
- IMsRdpClient9.put_DesktopHeight
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4e55d5a1f529435f0cdf6db3dcf801e7f24dda1a69e0bc1cad393942b672d4a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119513104"
---
# <a name="imstscaxdesktopheight-property"></a>Имстскакс: свойство Есктофеигхт:D

Задает высоту текущего элемента управления в пикселях на начальном удаленном рабочем столе.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_DesktopHeight(
  [in]  LONG newVal
);

HRESULT get_DesktopHeight(
  [out] LONG *pVal
);
```



## <a name="property-value"></a>Значение свойства

Новая высота (в пикселях).

## <a name="error-codes"></a>Коды ошибок

В случае успеха возвратите значение **\_ ОК** .

## <a name="remarks"></a>Remarks

задание свойства **десктофеигхт** является необязательным, но его необходимо задать перед вызовом метода [**Подключение**](imstscax-connect.md) . Если высота рабочего стола не указана или имеет значение 0, высота рабочего стола устанавливается равным высоте элемента управления. Минимальное и максимальное значения зависят от версии операционной системы клиента удаленный рабочий стол.

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

После установки соединения любые изменения высоты элемента управления не изменяют высоту удаленного рабочего стола. Вместо этого элемент управления выводит полосу прокрутки или центрирует удаленный рабочий стол по мере необходимости. Чтобы изменить размер рабочего стола активного подключения, используйте метод [**IMsRdpClient8:: Reconnect**](imsrdpclient8-reconnect.md) .

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

 

 





