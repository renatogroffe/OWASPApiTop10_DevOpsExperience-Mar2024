# APIM-MicrosoftEntra-ValidateJWT
Exemplo com configuracões para validar o Access Token de uma aplicação utilizando a policy &lt;validate-azure-ad-token> do Azure API Management e uma App Registration do Microsoft Entra ID.

Inclui script .http para testes com a extensão REST Client do VS Code.

Exemplo de uso da policy **&lt;validate-azure-ad-token>** (**inbound**):

```xml
    <inbound>
        <base />
        <validate-azure-ad-token tenant-id="id_tenant_microsofentraid">
            <client-application-ids>
                <application-id>id_appregistration</application-id>
            </client-application-ids>
        </validate-azure-ad-token>
    </inbound>
```



Para saber mais sobre a policy **&lt;validate-azure-ad-token>** acesse:

**https://learn.microsoft.com/en-us/azure/api-management/validate-azure-ad-token-policy**