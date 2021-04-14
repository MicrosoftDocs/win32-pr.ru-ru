---
title: Имсрдпклиентадванцедсеттингс Лоадбаланцеинфо, свойство
description: Указывает файл cookie балансировки нагрузки, который будет помещен в пакет запроса на подключение X. 224 в последовательности подключений протокола сервера узла сеансов удаленный рабочий стол (узел сеансов удаленных рабочих столов).
ms.assetid: 25f12a2e-00a2-42a8-afd3-81efcd94da94
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Лоадбаланцеинфо
- Службы удаленных рабочих столов свойства Лоадбаланцеинфо, интерфейс Имсрдпклиентадванцедсеттингс
- Службы удаленных рабочих столов интерфейса Имсрдпклиентадванцедсеттингс, свойство Лоадбаланцеинфо
- Службы удаленных рабочих столов свойства Лоадбаланцеинфо, интерфейс IMsRdpClientAdvancedSettings2
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings2, свойство Лоадбаланцеинфо
- Службы удаленных рабочих столов свойства Лоадбаланцеинфо, интерфейс IMsRdpClientAdvancedSettings3
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings3, свойство Лоадбаланцеинфо
- Службы удаленных рабочих столов свойства Лоадбаланцеинфо, интерфейс IMsRdpClientAdvancedSettings4
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings4, свойство Лоадбаланцеинфо
- Службы удаленных рабочих столов свойства Лоадбаланцеинфо, интерфейс IMsRdpClientAdvancedSettings5
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings5, свойство Лоадбаланцеинфо
- Службы удаленных рабочих столов свойства Лоадбаланцеинфо, интерфейс IMsRdpClientAdvancedSettings6
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings6, свойство Лоадбаланцеинфо
- Службы удаленных рабочих столов свойства Лоадбаланцеинфо, интерфейс IMsRdpClientAdvancedSettings7
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings7, свойство Лоадбаланцеинфо
- Службы удаленных рабочих столов свойства Лоадбаланцеинфо, интерфейс IMsRdpClientAdvancedSettings8
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings8, свойство Лоадбаланцеинфо
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.LoadBalanceInfo
- IMsRdpClientAdvancedSettings.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings.put_LoadBalanceInfo
- IMsRdpClientAdvancedSettings2.LoadBalanceInfo
- IMsRdpClientAdvancedSettings2.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings2.put_LoadBalanceInfo
- IMsRdpClientAdvancedSettings3.LoadBalanceInfo
- IMsRdpClientAdvancedSettings3.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings3.put_LoadBalanceInfo
- IMsRdpClientAdvancedSettings4.LoadBalanceInfo
- IMsRdpClientAdvancedSettings4.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings4.put_LoadBalanceInfo
- IMsRdpClientAdvancedSettings5.LoadBalanceInfo
- IMsRdpClientAdvancedSettings5.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings5.put_LoadBalanceInfo
- IMsRdpClientAdvancedSettings6.LoadBalanceInfo
- IMsRdpClientAdvancedSettings6.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings6.put_LoadBalanceInfo
- IMsRdpClientAdvancedSettings7.LoadBalanceInfo
- IMsRdpClientAdvancedSettings7.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings7.put_LoadBalanceInfo
- IMsRdpClientAdvancedSettings8.LoadBalanceInfo
- IMsRdpClientAdvancedSettings8.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings8.put_LoadBalanceInfo
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a12112eb2a18d38993e905f8d36175f1ab15f58a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415184"
---
# <a name="imsrdpclientadvancedsettingsloadbalanceinfo-property"></a>Свойство Имсрдпклиентадванцедсеттингс:: Лоадбаланцеинфо

Указывает файл cookie балансировки нагрузки, который будет помещен в пакет запроса на подключение X. 224 в последовательности подключений протокола сервера узла сеансов удаленный рабочий стол (узел сеансов удаленных рабочих столов).

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_LoadBalanceInfo(
  [in]  BSTR newLBInfo
);

HRESULT get_LoadBalanceInfo(
  [out] BSTR *pLBInfo
);
```



## <a name="property-value"></a>Значение свойства

Указатель на новый файл cookie. Дополнительные сведения см. в разделе "Примечания".

## <a name="error-codes"></a>Коды ошибок

При успешном выполнении возвращает значение **\_ ОК** .

## <a name="remarks"></a>Комментарии

Сведения о балансировке нагрузки используются маршрутизаторами балансировки нагрузки для выбора наиболее подходящего сервера для клиента при использовании ферм серверов узлов сеансов удаленных рабочих столов. Сам сервер узла сеансов удаленных рабочих столов не использует эти сведения и будет удален.

Файл cookie использует следующий синтаксис с учетом регистра:

**Файл cookie: МСТС =**_ипаддрессандпортнумбер_*_\\ r \\ n_*

Где *ипаддрессандпортнумбер* — это IP-адрес и номер порта в сетевом порядке байтов.

Например, файл cookie, используемый для доступа к IP-адресу 172.31.249.216, номер порта 3389 выглядит следующим образом:

**Файл cookie: МСТС = 3640205228.15629.0000 \\ r \\ n**

Последние четыре нуля являются необязательными и зарезервированы. Последняя десятичная запятая является обязательной, как и завершающий возврат каретки и перевод строки. Длина строки в символах должна быть кратной 2, поэтому при необходимости добавьте пробел.

Если файл cookie не указан, по умолчанию используется **файл cookie: мстшаш =**_username_*_\\ r \\ n_*.

Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                        |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                                  |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>          |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>          |
| IID<br/>                      | IID \_ имсрдпклиентадванцедсеттингс определен как 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2<br/> |



## <a name="see-also"></a>См. также раздел

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

 

 





