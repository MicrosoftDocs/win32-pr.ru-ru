---
title: Имсрдпклиентадванцедсеттингс Хоткэйалттаб, свойство
description: Указывает код виртуального ключа, добавляемый к ALT для определения замены сочетания клавиш для ALT + TAB.
ms.assetid: d7066fb4-f53f-4e55-ba12-fb4078ece144
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Хоткэйалттаб
- Службы удаленных рабочих столов свойства Хоткэйалттаб, интерфейс Имсрдпклиентадванцедсеттингс
- Службы удаленных рабочих столов интерфейса Имсрдпклиентадванцедсеттингс, свойство Хоткэйалттаб
- Службы удаленных рабочих столов свойства Хоткэйалттаб, интерфейс IMsRdpClientAdvancedSettings2
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings2, свойство Хоткэйалттаб
- Службы удаленных рабочих столов свойства Хоткэйалттаб, интерфейс IMsRdpClientAdvancedSettings3
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings3, свойство Хоткэйалттаб
- Службы удаленных рабочих столов свойства Хоткэйалттаб, интерфейс IMsRdpClientAdvancedSettings4
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings4, свойство Хоткэйалттаб
- Службы удаленных рабочих столов свойства Хоткэйалттаб, интерфейс IMsRdpClientAdvancedSettings5
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings5, свойство Хоткэйалттаб
- Службы удаленных рабочих столов свойства Хоткэйалттаб, интерфейс IMsRdpClientAdvancedSettings6
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings6, свойство Хоткэйалттаб
- Службы удаленных рабочих столов свойства Хоткэйалттаб, интерфейс IMsRdpClientAdvancedSettings7
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings7, свойство Хоткэйалттаб
- Службы удаленных рабочих столов свойства Хоткэйалттаб, интерфейс IMsRdpClientAdvancedSettings8
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings8, свойство Хоткэйалттаб
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.HotKeyAltTab
- IMsRdpClientAdvancedSettings.get_HotKeyAltTab
- IMsRdpClientAdvancedSettings.put_HotKeyAltTab
- IMsRdpClientAdvancedSettings2.HotKeyAltTab
- IMsRdpClientAdvancedSettings2.get_HotKeyAltTab
- IMsRdpClientAdvancedSettings2.put_HotKeyAltTab
- IMsRdpClientAdvancedSettings3.HotKeyAltTab
- IMsRdpClientAdvancedSettings3.get_HotKeyAltTab
- IMsRdpClientAdvancedSettings3.put_HotKeyAltTab
- IMsRdpClientAdvancedSettings4.HotKeyAltTab
- IMsRdpClientAdvancedSettings4.get_HotKeyAltTab
- IMsRdpClientAdvancedSettings4.put_HotKeyAltTab
- IMsRdpClientAdvancedSettings5.HotKeyAltTab
- IMsRdpClientAdvancedSettings5.get_HotKeyAltTab
- IMsRdpClientAdvancedSettings5.put_HotKeyAltTab
- IMsRdpClientAdvancedSettings6.HotKeyAltTab
- IMsRdpClientAdvancedSettings6.get_HotKeyAltTab
- IMsRdpClientAdvancedSettings6.put_HotKeyAltTab
- IMsRdpClientAdvancedSettings7.HotKeyAltTab
- IMsRdpClientAdvancedSettings7.get_HotKeyAltTab
- IMsRdpClientAdvancedSettings7.put_HotKeyAltTab
- IMsRdpClientAdvancedSettings8.HotKeyAltTab
- IMsRdpClientAdvancedSettings8.get_HotKeyAltTab
- IMsRdpClientAdvancedSettings8.put_HotKeyAltTab
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e22b50679b98bb57f40108287a303de3097cfe0bb3dc2fd552a957dae6479b1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120009894"
---
# <a name="imsrdpclientadvancedsettingshotkeyalttab-property"></a>Свойство Имсрдпклиентадванцедсеттингс:: Хоткэйалттаб

Указывает код виртуального ключа, добавляемый к ALT для определения замены сочетания клавиш для ALT + TAB.

Это свойство допустимо, только если свойство [**кэйбоардхукмоде**](imsrdpclientsecuredsettings-keyboardhookmode.md) не включено.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_HotKeyAltTab(
  [in]  LONG hotKeyAltTab
);

HRESULT get_HotKeyAltTab(
  [out] LONG *photKeyAltTab
);
```



## <a name="property-value"></a>Значение свойства

Новый код виртуального ключа. **VK \_ РАНЬШЕ** используется значение по умолчанию, а в результирующей последовательности — Alt + Page Up.

## <a name="error-codes"></a>Коды ошибок

При успешном выполнении возвращает значение **\_ ОК** .

## <a name="remarks"></a>Remarks

Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                        |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                                  |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>          |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>          |
| IID<br/>                      | IID \_ имсрдпклиентадванцедсеттингс определен как 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings3**](imstscadvancedsettings-interface.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**имсрдпклиентадванцедсеттингс**](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





