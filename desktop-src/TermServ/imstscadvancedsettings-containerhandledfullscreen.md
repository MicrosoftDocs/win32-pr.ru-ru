---
title: Имстскадванцедсеттингс Контаинерхандледфуллскрин, свойство
description: Указывает, включен ли полноэкранный режим, обрабатываемый контейнером.
ms.assetid: 67679323-4a74-4d91-abd0-607415295f3d
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Контаинерхандледфуллскрин
- Службы удаленных рабочих столов свойства Контаинерхандледфуллскрин, интерфейс Имстскадванцедсеттингс
- Службы удаленных рабочих столов интерфейса Имстскадванцедсеттингс, свойство Контаинерхандледфуллскрин
- Службы удаленных рабочих столов свойства Контаинерхандледфуллскрин, интерфейс Имсрдпклиентадванцедсеттингс
- Службы удаленных рабочих столов интерфейса Имсрдпклиентадванцедсеттингс, свойство Контаинерхандледфуллскрин
- Службы удаленных рабочих столов свойства Контаинерхандледфуллскрин, интерфейс IMsRdpClientAdvancedSettings2
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings2, свойство Контаинерхандледфуллскрин
- Службы удаленных рабочих столов свойства Контаинерхандледфуллскрин, интерфейс IMsRdpClientAdvancedSettings3
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings3, свойство Контаинерхандледфуллскрин
- Службы удаленных рабочих столов свойства Контаинерхандледфуллскрин, интерфейс IMsRdpClientAdvancedSettings4
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings4, свойство Контаинерхандледфуллскрин
- Службы удаленных рабочих столов свойства Контаинерхандледфуллскрин, интерфейс IMsRdpClientAdvancedSettings5
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings5, свойство Контаинерхандледфуллскрин
- Службы удаленных рабочих столов свойства Контаинерхандледфуллскрин, интерфейс IMsRdpClientAdvancedSettings6
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings6, свойство Контаинерхандледфуллскрин
- Службы удаленных рабочих столов свойства Контаинерхандледфуллскрин, интерфейс IMsRdpClientAdvancedSettings7
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings7, свойство Контаинерхандледфуллскрин
- Службы удаленных рабочих столов свойства Контаинерхандледфуллскрин, интерфейс IMsRdpClientAdvancedSettings8
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings8, свойство Контаинерхандледфуллскрин
topic_type:
- apiref
api_name:
- IMsTscAdvancedSettings.ContainerHandledFullScreen
- IMsTscAdvancedSettings.get_ContainerHandledFullScreen
- IMsTscAdvancedSettings.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings2.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings2.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings2.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings3.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings3.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings3.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings4.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings4.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings4.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings5.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings5.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings5.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings6.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings6.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings6.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings7.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings7.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings7.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings8.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings8.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings8.put_ContainerHandledFullScreen
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a7442ce16e2ff30ca2d9b3bd529d37382d1df41
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415764"
---
# <a name="imstscadvancedsettingscontainerhandledfullscreen-property"></a>Свойство Имстскадванцедсеттингс:: Контаинерхандледфуллскрин

Указывает, включен ли полноэкранный режим, обрабатываемый контейнером.

> [!Note]  
> Значение свойства **контаинерхандледфуллскрин** не действует, если элемент управления ActiveX удаленный рабочий стол является надежным для сценариев, и при попытке изменить значение возвращается **\_ false** .

 

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_ContainerHandledFullScreen(
  [in]  BOOL ContainerHandledFullScreen
);

HRESULT get_ContainerHandledFullScreen(
  [out] BOOL *pContainerHandledFullScreen
);
```



## <a name="property-value"></a>Значение свойства

Задайте для этого параметра значение **true** , чтобы включить режим или другое значение для отключения режима.

## <a name="error-codes"></a>Коды ошибок

При успешном выполнении возвращает значение **\_ ОК** . Возвращает **\_ значение false** , если не поддерживается.

## <a name="remarks"></a>Комментарии

Если этот режим включен, текущий контейнер обрабатывает переключение в полноэкранный режим и из него. Этот метод следует использовать, только если текущему контейнеру требуется обширный контроль над режимом полноэкранного режима. Если это свойство задано, элемент управления не вводит или не оставляет полноэкранный режим в ответ на сочетание клавиш в полноэкранном режиме (CTRL + ALT + BREAK); Вместо этого вызываются события [**имстскаксевентс:: онрекуестгофуллскрин**](imstscaxevents-onrequestgofullscreen.md) и [**Имстскаксевентс:: онрекуестлеавефуллскрин**](imstscaxevents-onrequestleavefullscreen.md) . Дополнительные сведения об этих событиях см. в разделе [**имстскаксевентс**](imstscaxevents-interface.md) .

Большинству приложений-контейнеров не нужно использовать полноэкранный режим, работающий в контейнере.

Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                  |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                            |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| IID<br/>                      | IID \_ имстскадванцедсеттингс определен как 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**имсрдпклиентадванцедсеттингс**](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md)
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

[**имстскадванцедсеттингс**](imstscadvancedsettings-interface.md)
</dt> </dl>

 

 





